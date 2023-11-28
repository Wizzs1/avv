### Views.py

		def index(request):
		    cars = Car.objects.all()
		    return render(request, "index.html", {'cars':cars})
		
		def all_cars(request):
		    dealer = CarDealer.objects.filter(car_dealer=request.user).first()
		    cars = Car.objects.filter(car_dealer=dealer)
		    return render(request, "all_cars.html", {'cars':cars})
		
		def add_car(request):
		    if request.method == "POST":
		        car_name = request.POST['car_name']
		        city = request.POST['city']
		        image = request.FILES['image']
		        capacity = request.POST['capacity']
		        rent = request.POST['rent']
		        car_dealer = CarDealer.objects.get(car_dealer=request.user)
		        try:
		            location = Location.objects.get(city=city)
		        except:
		            location = None
		        if location is not None:
		            car = Car(name=car_name, car_dealer=car_dealer, location=location, capacity=capacity, image=image, rent=rent)
		        else:
		            location = Location(city=city)
		            car = Car(name=car_name, car_dealer=car_dealer, location=location, capacity=capacity, image=image, rent=rent)
		        car.save()
		        alert = True
		        return render(request, "add_car.html", {'alert':alert})
		    return render(request, "add_car.html")
		
		def edit_car(request, myid):
		    car = Car.objects.filter(id=myid)[0]
		    if request.method == "POST":
		        car_name = request.POST['car_name']
		        city = request.POST['city']
		        capacity = request.POST['capacity']
		        rent = request.POST['rent']
		 
		        car.name = car_name
		        car.city = city
		        car.capacity = capacity
		        car.rent = rent
		        car.save()
		 
		        try:
		            image = request.FILES['image']
		            car.image = image
		            car.save()
		        except:
		            pass
		        alert = True
		        return render(request, "edit_car.html", {'alert':alert})
		    return render(request, "edit_car.html", {'car':car})
		
		def all_orders(request):
		    username = request.user
		    user = User.objects.get(username=username)
		    car_dealer = CarDealer.objects.get(car_dealer=user)
		    orders = Order.objects.filter(car_dealer=car_dealer)
		    all_orders = []
		    for order in orders:
		        if order.is_complete == False:
		            all_orders.append(order)
		    return render(request, "all_orders.html", {'all_orders':all_orders})
		
		def earnings(request):
		    username = request.user
		    user = User.objects.get(username=username)
		    car_dealer = CarDealer.objects.get(car_dealer=user)
		    orders = Order.objects.filter(car_dealer=car_dealer)
		    all_orders = []
		    for order in orders:
		        all_orders.append(order)
		    return render(request, "earnings.html", {'amount':car_dealer.earnings, 'all_orders':all_orders})
		
		def customer_homepage(request):
		    return render(request, "customer_homepage.html")
		
		def past_orders(request):
		    all_orders = []
		    user = User.objects.get(username=request.user)
		    try:
		        orders = Order.objects.filter(user=user)
		    except:
		        orders = None
		    if orders is not None:
		        for order in orders:
		            if order.is_complete == False:
		                order_dictionary = {'id':order.id, 'rent':order.rent, 'car':order.car, 'days':order.days, 'car_dealer':order.car_dealer}
		                all_orders.append(order_dictionary)
		    return render(request, "past_orders.html", {'all_orders':all_orders})
