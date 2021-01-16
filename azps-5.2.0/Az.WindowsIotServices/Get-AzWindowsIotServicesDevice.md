---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: b9236dc7c3e4a12c9be6b72cd63874044ee49065
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260589"
---
# <span data-ttu-id="d3a95-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="d3a95-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="d3a95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3a95-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a95-103">Obter os metadados relacionados a não segurança de um serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="d3a95-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="d3a95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3a95-104">SYNTAX</span></span>

### <span data-ttu-id="d3a95-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3a95-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3a95-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d3a95-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3a95-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d3a95-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3a95-108">Programação</span><span class="sxs-lookup"><span data-stu-id="d3a95-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d3a95-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3a95-109">DESCRIPTION</span></span>
<span data-ttu-id="d3a95-110">Obter os metadados relacionados a não segurança de um serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="d3a95-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="d3a95-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3a95-111">EXAMPLES</span></span>

### <span data-ttu-id="d3a95-112">Exemplo 1: obter todos os serviços IoT do Windows em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d3a95-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="d3a95-113">Este comando obtém todos os serviços da Windows IoT em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d3a95-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="d3a95-114">Exemplo 2: obter todos os serviços IoT do Windows em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d3a95-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="d3a95-115">Este comando obtém todos os serviços da Windows IoT em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3a95-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="d3a95-116">Exemplo 3: obter um serviço Windows IoT por nome</span><span class="sxs-lookup"><span data-stu-id="d3a95-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="d3a95-117">Este comando obtém um serviço Windows IoT por nome.</span><span class="sxs-lookup"><span data-stu-id="d3a95-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="d3a95-118">Exemplo 4: obter um serviço de IoT do Windows por objeto</span><span class="sxs-lookup"><span data-stu-id="d3a95-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="d3a95-119">Esse comando obtém um serviço Windows IoT por objeto.</span><span class="sxs-lookup"><span data-stu-id="d3a95-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="d3a95-120">Exemplo 4: obter um serviço de IoT do Windows por pipeline</span><span class="sxs-lookup"><span data-stu-id="d3a95-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="d3a95-121">Esse comando obtém um serviço Windows IoT por pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3a95-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="d3a95-122">OS</span><span class="sxs-lookup"><span data-stu-id="d3a95-122">PARAMETERS</span></span>

### <span data-ttu-id="d3a95-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a95-123">-DefaultProfile</span></span>
<span data-ttu-id="d3a95-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a95-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a95-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3a95-125">-InputObject</span></span>
<span data-ttu-id="d3a95-126">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d3a95-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d3a95-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3a95-127">-Name</span></span>
<span data-ttu-id="d3a95-128">O nome do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="d3a95-128">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="d3a95-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a95-129">-ResourceGroupName</span></span>
<span data-ttu-id="d3a95-130">O nome do grupo de recursos que contém o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="d3a95-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="d3a95-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3a95-131">-SubscriptionId</span></span>
<span data-ttu-id="d3a95-132">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d3a95-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="d3a95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a95-133">CommonParameters</span></span>
<span data-ttu-id="d3a95-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a95-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3a95-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a95-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3a95-136">INPUTS</span></span>

### <span data-ttu-id="d3a95-137">Microsoft. Azure. PowerShell. cmdlets. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="d3a95-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="d3a95-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3a95-138">OUTPUTS</span></span>

### <span data-ttu-id="d3a95-139">Microsoft. Azure. PowerShell. cmdlets. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="d3a95-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="d3a95-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3a95-140">NOTES</span></span>

<span data-ttu-id="d3a95-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d3a95-141">ALIASES</span></span>

<span data-ttu-id="d3a95-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d3a95-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d3a95-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d3a95-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3a95-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d3a95-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d3a95-145">INPUTobject <IWindowsIotServicesIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d3a95-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3a95-146">`[DeviceName <String>]`: O nome do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="d3a95-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="d3a95-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d3a95-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3a95-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="d3a95-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="d3a95-149">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d3a95-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="d3a95-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3a95-150">RELATED LINKS</span></span>

