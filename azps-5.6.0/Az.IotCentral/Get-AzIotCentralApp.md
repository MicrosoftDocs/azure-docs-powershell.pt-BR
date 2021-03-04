---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 2d79857df255bb960c51b87c536013921f3b1c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891378"
---
# <span data-ttu-id="8cad9-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="8cad9-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="8cad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cad9-102">SYNOPSIS</span></span>
<span data-ttu-id="8cad9-103">Obtém propriedades para um ou vários Aplicativos Centrais de IoT.</span><span class="sxs-lookup"><span data-stu-id="8cad9-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="8cad9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8cad9-104">SYNTAX</span></span>

### <span data-ttu-id="8cad9-105">ListIotCentralAppsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8cad9-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cad9-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cad9-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cad9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cad9-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cad9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8cad9-108">DESCRIPTION</span></span>
<span data-ttu-id="8cad9-109">Obtém os metadados para um Aplicativo Central de IoT específico ou todos os aplicativos em um Grupo de Recursos ou Assinatura, dependendo do Conjunto de Parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8cad9-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="8cad9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cad9-110">EXAMPLES</span></span>

### <span data-ttu-id="8cad9-111">Exemplo 1 Obter Aplicativo Central de IoT específico.</span><span class="sxs-lookup"><span data-stu-id="8cad9-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="8cad9-112">Obtém os metadados do Aplicativo Central de IoT especificado.</span><span class="sxs-lookup"><span data-stu-id="8cad9-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="8cad9-113">Saída de Exemplo:</span><span class="sxs-lookup"><span data-stu-id="8cad9-113">Example Output:</span></span>

<span data-ttu-id="8cad9-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Nome : MyAppResourceName Tipo : Microsoft.IoTCentral/IoTApps Local : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cad9-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="8cad9-115">Exemplo 2 Get IoT Central Applications in Subscription.</span><span class="sxs-lookup"><span data-stu-id="8cad9-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="8cad9-116">Obtém os metadados de todos os Aplicativos Centrais de IoT na Assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8cad9-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="8cad9-117">Saída de Exemplo:</span><span class="sxs-lookup"><span data-stu-id="8cad9-117">Example Output:</span></span>

<span data-ttu-id="8cad9-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Nome : MyAppResourceName Tipo : Microsoft.IoTCentral/IoTApps Local : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cad9-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="8cad9-119">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Nome : MyAppResourceName2 Tipo : Microsoft.IoTCentral/IoTApps Local : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="8cad9-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="8cad9-120">Exemplo 3 Obter Aplicativos Centrais de IoT no Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8cad9-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="8cad9-121">Obtém os metadados de todos os Aplicativos Centrais de IoT no Grupo de Recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="8cad9-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="8cad9-122">Saída de Exemplo:</span><span class="sxs-lookup"><span data-stu-id="8cad9-122">Example Output:</span></span>

<span data-ttu-id="8cad9-123">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Nome : MyAppResourceName Tipo : Microsoft.IoTCentral/IoTApps Local : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cad9-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="8cad9-124">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Nome : MyAppResourceName2 Tipo : Microsoft.IoTCentral/IoTApps Local : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cad9-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="8cad9-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8cad9-125">PARAMETERS</span></span>

### <span data-ttu-id="8cad9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cad9-126">-DefaultProfile</span></span>
<span data-ttu-id="8cad9-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cad9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cad9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8cad9-128">-Name</span></span>
<span data-ttu-id="8cad9-129">Nome do Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="8cad9-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cad9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cad9-130">-ResourceGroupName</span></span>
<span data-ttu-id="8cad9-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8cad9-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cad9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cad9-132">-ResourceId</span></span>
<span data-ttu-id="8cad9-133">Id de Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="8cad9-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cad9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cad9-134">CommonParameters</span></span>
<span data-ttu-id="8cad9-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cad9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cad9-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cad9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cad9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8cad9-137">INPUTS</span></span>

### <span data-ttu-id="8cad9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8cad9-138">System.String</span></span>

## <span data-ttu-id="8cad9-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8cad9-139">OUTPUTS</span></span>

### <span data-ttu-id="8cad9-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="8cad9-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="8cad9-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="8cad9-141">NOTES</span></span>

## <span data-ttu-id="8cad9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cad9-142">RELATED LINKS</span></span>
