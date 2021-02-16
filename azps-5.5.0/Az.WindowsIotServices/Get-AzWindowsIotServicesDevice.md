---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: b9236dc7c3e4a12c9be6b72cd63874044ee49065
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118486"
---
# <span data-ttu-id="ed8f6-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="ed8f6-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="ed8f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8f6-103">Obter os metadados não relacionados à segurança de um Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="ed8f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed8f6-104">SYNTAX</span></span>

### <span data-ttu-id="ed8f6-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed8f6-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ed8f6-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ed8f6-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ed8f6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ed8f6-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed8f6-108">Lista</span><span class="sxs-lookup"><span data-stu-id="ed8f6-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ed8f6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed8f6-109">DESCRIPTION</span></span>
<span data-ttu-id="ed8f6-110">Obter os metadados não relacionados à segurança de um Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="ed8f6-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed8f6-111">EXAMPLES</span></span>

### <span data-ttu-id="ed8f6-112">Exemplo 1: Obter todos os serviços do Windows IoT em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="ed8f6-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="ed8f6-113">Esse comando obtém todos os serviços do Windows IoT sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="ed8f6-114">Exemplo 2: Obter todos os serviços de IoT do Windows em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ed8f6-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="ed8f6-115">Esse comando obtém todos os serviços de IoT do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="ed8f6-116">Exemplo 3: Obter um serviço de IoT do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="ed8f6-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="ed8f6-117">Esse comando obtém um serviço de IoT do Windows por nome.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="ed8f6-118">Exemplo 4: Obter um serviço de IoT do Windows por objeto</span><span class="sxs-lookup"><span data-stu-id="ed8f6-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="ed8f6-119">Esse comando obtém um serviço de IoT do Windows por objeto.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="ed8f6-120">Exemplo 4: Obter um serviço de IoT do Windows por pipeline</span><span class="sxs-lookup"><span data-stu-id="ed8f6-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="ed8f6-121">Esse comando obtém um serviço de IoT do Windows por pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="ed8f6-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed8f6-122">PARAMETERS</span></span>

### <span data-ttu-id="ed8f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8f6-123">-DefaultProfile</span></span>
<span data-ttu-id="ed8f6-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed8f6-125">-InputObject</span></span>
<span data-ttu-id="ed8f6-126">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f6-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed8f6-127">-Name</span></span>
<span data-ttu-id="ed8f6-128">O nome do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-128">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8f6-129">-ResourceGroupName</span></span>
<span data-ttu-id="ed8f6-130">O nome do grupo de recursos que contém o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f6-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed8f6-131">-SubscriptionId</span></span>
<span data-ttu-id="ed8f6-132">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-132">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8f6-133">CommonParameters</span></span>
<span data-ttu-id="ed8f6-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8f6-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed8f6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8f6-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="ed8f6-136">INPUTS</span></span>

### <span data-ttu-id="ed8f6-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="ed8f6-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="ed8f6-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="ed8f6-138">OUTPUTS</span></span>

### <span data-ttu-id="ed8f6-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="ed8f6-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="ed8f6-140">Notas</span><span class="sxs-lookup"><span data-stu-id="ed8f6-140">NOTES</span></span>

<span data-ttu-id="ed8f6-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="ed8f6-141">ALIASES</span></span>

<span data-ttu-id="ed8f6-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ed8f6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed8f6-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed8f6-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed8f6-145">INPUTOBJECT: <IWindowsIotServicesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="ed8f6-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ed8f6-146">`[DeviceName <String>]`: o nome do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="ed8f6-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ed8f6-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ed8f6-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="ed8f6-149">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ed8f6-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="ed8f6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed8f6-150">RELATED LINKS</span></span>

