
# Information dont on a besoin

- version Spring-boot
- version java
- configuration Hikari
- Est-ce qu'on a du cache Caffeine ?
- Est-ce que l'on mixe cache et Hikari

# Liste des applicaitons

- api-warehouse-availability-date
- api-warehouse-stock-level
- api-stock-external-supplier


# Exploration des logs
![[Pasted image 20231009153716.png]]

```
Retour searchProductWarehouseNextAvailabilityDate : class ProductWarehouseAvailabilityDate { product: class ProductRef { erpId: 187934 } warehouseId: ENTMLP availableOn: null }
```