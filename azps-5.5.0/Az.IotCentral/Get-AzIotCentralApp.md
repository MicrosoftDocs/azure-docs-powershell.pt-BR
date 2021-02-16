---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117615"
---
# <span data-ttu-id="e6093-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e6093-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="e6093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6093-102">SYNOPSIS</span></span>
<span data-ttu-id="e6093-103">Obtém propriedades para um ou vários Aplicativos Centrais de IoT.</span><span class="sxs-lookup"><span data-stu-id="e6093-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="e6093-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6093-104">SYNTAX</span></span>

### <span data-ttu-id="e6093-105">ListIotCentralAppsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e6093-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6093-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6093-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6093-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6093-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6093-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6093-108">DESCRIPTION</span></span>
<span data-ttu-id="e6093-109">Obtém os metadados de um Aplicativo Central de IoT específico ou todos os aplicativos em um Grupo de Recursos ou Assinatura, dependendo do Conjunto de Parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e6093-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="e6093-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e6093-110">EXAMPLES</span></span>

### <span data-ttu-id="e6093-111">Exemplo 1 Obter Aplicativo Central de IoT específico.</span><span class="sxs-lookup"><span data-stu-id="e6093-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="e6093-112">Obtém os metadados do Aplicativo Central de IoT especificado.</span><span class="sxs-lookup"><span data-stu-id="e6093-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="e6093-113">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="e6093-113">Example Output:</span></span>

<span data-ttu-id="e6093-114">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain iotc-default@1.0.0 Template : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6093-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="e6093-115">Exemplo 2 Obter Aplicativos Centrais de IoT em Assinatura.</span><span class="sxs-lookup"><span data-stu-id="e6093-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="e6093-116">Obtém os metadados de todos os Aplicativos Centrais de IoT na Assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e6093-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="e6093-117">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="e6093-117">Example Output:</span></span>

<span data-ttu-id="e6093-118">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain iotc-default@1.0.0 Template : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6093-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="e6093-119">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location: westus Tag: {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Meu subdomínio Nome de Exibição Personalizado 2 : Meu Modelo MyAppSubdomain2 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="e6093-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="e6093-120">Exemplo 3 Obter Aplicativos Centrais de IoT no Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e6093-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="e6093-121">Obtém os metadados de todos os Aplicativos Centrais de IoT no Grupo de Recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="e6093-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="e6093-122">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="e6093-122">Example Output:</span></span>

<span data-ttu-id="e6093-123">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain iotc-default@1.0.0 Template : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6093-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="e6093-124">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Meu subdomínio Nome de Exibição Personalizado 2 : Meu Modelo MyAppSubdomain2 : iotc-default@1.0.0 SubscriptionId : XXXXXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6093-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="e6093-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6093-125">PARAMETERS</span></span>

### <span data-ttu-id="e6093-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6093-126">-DefaultProfile</span></span>
<span data-ttu-id="e6093-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6093-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6093-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6093-128">-Name</span></span>
<span data-ttu-id="e6093-129">Nome do Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="e6093-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="e6093-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6093-130">-ResourceGroupName</span></span>
<span data-ttu-id="e6093-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e6093-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="e6093-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6093-132">-ResourceId</span></span>
<span data-ttu-id="e6093-133">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="e6093-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="e6093-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6093-134">CommonParameters</span></span>
<span data-ttu-id="e6093-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6093-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6093-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6093-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6093-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="e6093-137">INPUTS</span></span>

### <span data-ttu-id="e6093-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e6093-138">System.String</span></span>

## <span data-ttu-id="e6093-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="e6093-139">OUTPUTS</span></span>

### <span data-ttu-id="e6093-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e6093-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="e6093-141">Notas</span><span class="sxs-lookup"><span data-stu-id="e6093-141">NOTES</span></span>

## <span data-ttu-id="e6093-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6093-142">RELATED LINKS</span></span>
