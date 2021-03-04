---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: ffae73880f66e378c7270ba5ce3645eae63064ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891377"
---
# <span data-ttu-id="d8f25-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d8f25-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="d8f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f25-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f25-103">Cria um novo Aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="d8f25-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="d8f25-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d8f25-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f25-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8f25-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f25-106">Cria um novo Aplicativo Central de IoT com as propriedades e metadados fornecidos.</span><span class="sxs-lookup"><span data-stu-id="d8f25-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="d8f25-107">Para uma introdução à Central de IoT, consulte https://docs.microsoft.com/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="d8f25-107">For an introduction to IoT Central, see https://docs.microsoft.com/azure/iot-central/.</span></span>

## <span data-ttu-id="d8f25-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8f25-108">EXAMPLES</span></span>

### <span data-ttu-id="d8f25-109">Exemplo 1 Criar aplicativo central de IoT simples.</span><span class="sxs-lookup"><span data-stu-id="d8f25-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="d8f25-110">Saída de Exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8f25-110">Example Output:</span></span>

<span data-ttu-id="d8f25-111">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Nome : MyAppResourceName Tipo : Microsoft.IoTCentral/IoTApps Localização : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSku ApplicationIdInfo : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : MyAppResourceName Subdomínio : MyAppSubdomain Modelo : iotc-default@1.0.0 SubscriptionId : XXXXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f25-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="d8f25-112">Crie um aplicativo Central de IoT na camada de preços padrão ST2, na região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d8f25-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="d8f25-113">Exemplo 2 Criar aplicativo central de IoT simples.</span><span class="sxs-lookup"><span data-stu-id="d8f25-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="d8f25-114">Saída de Exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8f25-114">Example Output:</span></span>

<span data-ttu-id="d8f25-115">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Nome : MyAppResourceName Tipo : Microsoft.IoTCentral/IoTApps Localização : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppS ApplicationId dekuInfo : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f25-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="d8f25-116">Crie um aplicativo Central de IoT com a camada de preços padrão ST2 na região 'westus', com um nome de exibição personalizado, com base no modelo padrão do iotc.</span><span class="sxs-lookup"><span data-stu-id="d8f25-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="d8f25-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d8f25-117">PARAMETERS</span></span>

### <span data-ttu-id="d8f25-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8f25-118">-AsJob</span></span>
<span data-ttu-id="d8f25-119">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d8f25-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="d8f25-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f25-120">-DefaultProfile</span></span>
<span data-ttu-id="d8f25-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f25-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f25-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d8f25-122">-DisplayName</span></span>
<span data-ttu-id="d8f25-123">Nome de exibição personalizado para o aplicativo Central da IoT.</span><span class="sxs-lookup"><span data-stu-id="d8f25-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="d8f25-124">O padrão é o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8f25-124">Default is resource name.</span></span>

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

### <span data-ttu-id="d8f25-125">-Location</span><span class="sxs-lookup"><span data-stu-id="d8f25-125">-Location</span></span>
<span data-ttu-id="d8f25-126">Local do aplicativo Central da IoT.</span><span class="sxs-lookup"><span data-stu-id="d8f25-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="d8f25-127">Padrão é o local do grupo de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="d8f25-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="d8f25-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d8f25-128">-Name</span></span>
<span data-ttu-id="d8f25-129">Nome do Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="d8f25-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="d8f25-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f25-130">-ResourceGroupName</span></span>
<span data-ttu-id="d8f25-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d8f25-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="d8f25-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="d8f25-132">-Sku</span></span>
<span data-ttu-id="d8f25-133">Camada de preços para aplicativos IoT Central.</span><span class="sxs-lookup"><span data-stu-id="d8f25-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="d8f25-134">O valor padrão é ST2.</span><span class="sxs-lookup"><span data-stu-id="d8f25-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="d8f25-135">-Subdomínio</span><span class="sxs-lookup"><span data-stu-id="d8f25-135">-Subdomain</span></span>
<span data-ttu-id="d8f25-136">Subdomínio para a URL Central da IoT.</span><span class="sxs-lookup"><span data-stu-id="d8f25-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="d8f25-137">Cada aplicativo deve ter um subdomínio exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d8f25-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="d8f25-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8f25-138">-Tag</span></span>
<span data-ttu-id="d8f25-139">Iot Marcas de Recurso de Aplicativo Central.</span><span class="sxs-lookup"><span data-stu-id="d8f25-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="d8f25-140">-Template</span><span class="sxs-lookup"><span data-stu-id="d8f25-140">-Template</span></span>
<span data-ttu-id="d8f25-141">Nome do modelo de aplicativo central da IoT.</span><span class="sxs-lookup"><span data-stu-id="d8f25-141">IoT Central application template name.</span></span>
<span data-ttu-id="d8f25-142">O padrão é um aplicativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="d8f25-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="d8f25-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8f25-143">-Confirm</span></span>
<span data-ttu-id="d8f25-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f25-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f25-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f25-145">-WhatIf</span></span>
<span data-ttu-id="d8f25-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8f25-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f25-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8f25-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f25-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f25-148">CommonParameters</span></span>
<span data-ttu-id="d8f25-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f25-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f25-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8f25-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f25-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8f25-151">INPUTS</span></span>

### <span data-ttu-id="d8f25-152">System.String</span><span class="sxs-lookup"><span data-stu-id="d8f25-152">System.String</span></span>

### <span data-ttu-id="d8f25-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8f25-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8f25-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d8f25-154">OUTPUTS</span></span>

### <span data-ttu-id="d8f25-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d8f25-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="d8f25-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="d8f25-156">NOTES</span></span>

## <span data-ttu-id="d8f25-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8f25-157">RELATED LINKS</span></span>
