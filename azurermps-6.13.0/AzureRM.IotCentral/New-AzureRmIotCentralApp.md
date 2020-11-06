---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/new-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
ms.openlocfilehash: d0bb10324c1a97b6228a26a7ab079edb4845d48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441272"
---
# <span data-ttu-id="00f6e-101">New-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="00f6e-101">New-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="00f6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="00f6e-103">Cria um novo aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="00f6e-103">Creates a new IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00f6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00f6e-104">SYNTAX</span></span>

```
New-AzureRmIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00f6e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="00f6e-106">Cria um novo aplicativo Central de IoT com as propriedades e os metadados fornecidos.</span><span class="sxs-lookup"><span data-stu-id="00f6e-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="00f6e-107">Para obter uma introdução ao IoT central, consulte https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="00f6e-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="00f6e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00f6e-108">EXAMPLES</span></span>

### <span data-ttu-id="00f6e-109">Exemplo 1 Crie um aplicativo Central simples de IoT.</span><span class="sxs-lookup"><span data-stu-id="00f6e-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="00f6e-110">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="00f6e-110">Example Output:</span></span>

<span data-ttu-id="00f6e-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX iotc-default@1.0.0 -xxxx-xxxxxxxxxxxx MyAppResourceName: MyAppSubdomain de assinatura: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f6e-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="00f6e-112">Crie um aplicativo Central do IoT na camada de preços padrão S1, na região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00f6e-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="00f6e-113">Exemplo 2 crie um aplicativo Central simples de IoT.</span><span class="sxs-lookup"><span data-stu-id="00f6e-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="00f6e-114">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="00f6e-114">Example Output:</span></span>

<span data-ttu-id="00f6e-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu nome de exibição personalizado subdomínio: MyAppSubdomain modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f6e-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="00f6e-116">Crie um aplicativo Central do IoT com o tipo de preço padrão S1 na região ' oesteus ', com um nome de exibição personalizado, com base no modelo IOTC-padrão.</span><span class="sxs-lookup"><span data-stu-id="00f6e-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="00f6e-117">OS</span><span class="sxs-lookup"><span data-stu-id="00f6e-117">PARAMETERS</span></span>

### <span data-ttu-id="00f6e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00f6e-118">-AsJob</span></span>
<span data-ttu-id="00f6e-119">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="00f6e-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f6e-120">-DefaultProfile</span></span>
<span data-ttu-id="00f6e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00f6e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="00f6e-122">-DisplayName</span></span>
<span data-ttu-id="00f6e-123">Nome de exibição personalizado para o aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="00f6e-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="00f6e-124">O padrão é o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="00f6e-124">Default is resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-125">-Local</span><span class="sxs-lookup"><span data-stu-id="00f6e-125">-Location</span></span>
<span data-ttu-id="00f6e-126">Localização do seu aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="00f6e-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="00f6e-127">Padrão é o local do grupo de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="00f6e-127">Default is the location of target resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="00f6e-128">-Name</span></span>
<span data-ttu-id="00f6e-129">Nome do recurso de aplicativo da central do IOT.</span><span class="sxs-lookup"><span data-stu-id="00f6e-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f6e-130">-ResourceGroupName</span></span>
<span data-ttu-id="00f6e-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00f6e-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="00f6e-132">-Sku</span></span>
<span data-ttu-id="00f6e-133">Tipo de preço para aplicativos da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="00f6e-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="00f6e-134">O valor padrão é S1.</span><span class="sxs-lookup"><span data-stu-id="00f6e-134">Default value is S1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-135">-Subdomínio</span><span class="sxs-lookup"><span data-stu-id="00f6e-135">-Subdomain</span></span>
<span data-ttu-id="00f6e-136">Subdomínio para a URL do centro da IoT.</span><span class="sxs-lookup"><span data-stu-id="00f6e-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="00f6e-137">Cada aplicativo deve ter um subdomínio exclusivo.</span><span class="sxs-lookup"><span data-stu-id="00f6e-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="00f6e-138">-Tag</span></span>
<span data-ttu-id="00f6e-139">Marcas de recursos de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="00f6e-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-140">-Modelo</span><span class="sxs-lookup"><span data-stu-id="00f6e-140">-Template</span></span>
<span data-ttu-id="00f6e-141">Nome do modelo de aplicativo do IoT central.</span><span class="sxs-lookup"><span data-stu-id="00f6e-141">IoT Central application template name.</span></span>
<span data-ttu-id="00f6e-142">O padrão é um aplicativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="00f6e-142">Default is a custom application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00f6e-143">-Confirm</span></span>
<span data-ttu-id="00f6e-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00f6e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00f6e-145">-WhatIf</span></span>
<span data-ttu-id="00f6e-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00f6e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00f6e-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00f6e-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f6e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f6e-148">CommonParameters</span></span>
<span data-ttu-id="00f6e-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f6e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f6e-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f6e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f6e-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00f6e-151">INPUTS</span></span>

### <span data-ttu-id="00f6e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="00f6e-152">System.String</span></span>
### <span data-ttu-id="00f6e-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="00f6e-153">System.Collections.Hashtable</span></span>
## <span data-ttu-id="00f6e-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00f6e-154">OUTPUTS</span></span>

### <span data-ttu-id="00f6e-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="00f6e-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="00f6e-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00f6e-156">NOTES</span></span>

## <span data-ttu-id="00f6e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00f6e-157">RELATED LINKS</span></span>
