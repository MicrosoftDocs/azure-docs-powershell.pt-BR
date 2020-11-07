---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: af622bbbed98a897df1774303f1417723ebfb32c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777353"
---
# <span data-ttu-id="cb377-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="cb377-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="cb377-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb377-102">SYNOPSIS</span></span>
<span data-ttu-id="cb377-103">Cria um novo aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="cb377-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="cb377-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb377-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb377-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb377-105">DESCRIPTION</span></span>
<span data-ttu-id="cb377-106">Cria um novo aplicativo Central de IoT com as propriedades e os metadados fornecidos.</span><span class="sxs-lookup"><span data-stu-id="cb377-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="cb377-107">Para obter uma introdução ao IoT central, consulte https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="cb377-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="cb377-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb377-108">EXAMPLES</span></span>

### <span data-ttu-id="cb377-109">Exemplo 1 Crie um aplicativo Central simples de IoT.</span><span class="sxs-lookup"><span data-stu-id="cb377-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="cb377-110">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="cb377-110">Example Output:</span></span>

<span data-ttu-id="cb377-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX iotc-default@1.0.0 -xxxx-xxxxxxxxxxxx MyAppResourceName: MyAppSubdomain de assinatura: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb377-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="cb377-112">Crie um aplicativo da central do IoT na faixa de preços padrão ST2, na região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb377-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="cb377-113">Exemplo 2 crie um aplicativo Central simples de IoT.</span><span class="sxs-lookup"><span data-stu-id="cb377-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="cb377-114">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="cb377-114">Example Output:</span></span>

<span data-ttu-id="cb377-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu nome de exibição personalizado subdomínio: MyAppSubdomain modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb377-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="cb377-116">Crie um aplicativo Central do IoT com o tipo de preço padrão ST2 na região ' oesteus ', com um nome de exibição personalizado, com base no modelo IOTC-padrão.</span><span class="sxs-lookup"><span data-stu-id="cb377-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="cb377-117">OS</span><span class="sxs-lookup"><span data-stu-id="cb377-117">PARAMETERS</span></span>

### <span data-ttu-id="cb377-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb377-118">-AsJob</span></span>
<span data-ttu-id="cb377-119">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="cb377-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb377-120">-DefaultProfile</span></span>
<span data-ttu-id="cb377-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb377-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb377-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cb377-122">-DisplayName</span></span>
<span data-ttu-id="cb377-123">Nome de exibição personalizado para o aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="cb377-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="cb377-124">O padrão é o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="cb377-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-125">-Local</span><span class="sxs-lookup"><span data-stu-id="cb377-125">-Location</span></span>
<span data-ttu-id="cb377-126">Localização do seu aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="cb377-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="cb377-127">Padrão é o local do grupo de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="cb377-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb377-128">-Name</span></span>
<span data-ttu-id="cb377-129">Nome do recurso de aplicativo da central do IOT.</span><span class="sxs-lookup"><span data-stu-id="cb377-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb377-130">-ResourceGroupName</span></span>
<span data-ttu-id="cb377-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb377-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="cb377-132">-Sku</span></span>
<span data-ttu-id="cb377-133">Tipo de preço para aplicativos da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="cb377-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="cb377-134">O valor padrão é ST2.</span><span class="sxs-lookup"><span data-stu-id="cb377-134">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-135">-Subdomínio</span><span class="sxs-lookup"><span data-stu-id="cb377-135">-Subdomain</span></span>
<span data-ttu-id="cb377-136">Subdomínio para a URL do centro da IoT.</span><span class="sxs-lookup"><span data-stu-id="cb377-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="cb377-137">Cada aplicativo deve ter um subdomínio exclusivo.</span><span class="sxs-lookup"><span data-stu-id="cb377-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="cb377-138">-Tag</span></span>
<span data-ttu-id="cb377-139">Marcas de recursos de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="cb377-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-140">-Modelo</span><span class="sxs-lookup"><span data-stu-id="cb377-140">-Template</span></span>
<span data-ttu-id="cb377-141">Nome do modelo de aplicativo do IoT central.</span><span class="sxs-lookup"><span data-stu-id="cb377-141">IoT Central application template name.</span></span>
<span data-ttu-id="cb377-142">O padrão é um aplicativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="cb377-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb377-143">-Confirm</span></span>
<span data-ttu-id="cb377-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb377-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb377-145">-WhatIf</span></span>
<span data-ttu-id="cb377-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb377-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb377-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb377-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb377-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb377-148">CommonParameters</span></span>
<span data-ttu-id="cb377-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb377-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb377-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb377-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb377-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb377-151">INPUTS</span></span>

### <span data-ttu-id="cb377-152">System. String</span><span class="sxs-lookup"><span data-stu-id="cb377-152">System.String</span></span>

### <span data-ttu-id="cb377-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cb377-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cb377-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb377-154">OUTPUTS</span></span>

### <span data-ttu-id="cb377-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="cb377-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="cb377-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb377-156">NOTES</span></span>

## <span data-ttu-id="cb377-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb377-157">RELATED LINKS</span></span>
