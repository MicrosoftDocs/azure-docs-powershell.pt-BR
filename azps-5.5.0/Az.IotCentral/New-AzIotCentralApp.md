---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113629"
---
# <span data-ttu-id="2df54-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="2df54-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="2df54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2df54-102">SYNOPSIS</span></span>
<span data-ttu-id="2df54-103">Cria um novo Aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="2df54-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="2df54-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2df54-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df54-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2df54-105">DESCRIPTION</span></span>
<span data-ttu-id="2df54-106">Cria um novo Aplicativo Central de IoT com as propriedades e metadados fornecidos.</span><span class="sxs-lookup"><span data-stu-id="2df54-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="2df54-107">Para uma introdução à Central de IoT, consulte https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="2df54-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="2df54-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2df54-108">EXAMPLES</span></span>

### <span data-ttu-id="2df54-109">Exemplo 1 Criar aplicativo central de IoT simples.</span><span class="sxs-lookup"><span data-stu-id="2df54-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="2df54-110">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="2df54-110">Example Output:</span></span>

<span data-ttu-id="2df54-111">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSku ApplicationIdinfo : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : MyAppResourceName Subdomain : iotc-default@1.0.0 MyAppSubdomain Template : SubscriptionId : XXXXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX RESOURCEGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df54-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="2df54-112">Crie um aplicativo Central de IoT no nível de preços padrão ST2, na região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2df54-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="2df54-113">Exemplo 2 Criar aplicativo central de IoT simples.</span><span class="sxs-lookup"><span data-stu-id="2df54-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="2df54-114">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="2df54-114">Example Output:</span></span>

<span data-ttu-id="2df54-115">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSKuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Meu subdomínio de nome de exibição personalizado : iotc-default@1.0.0 MeuAppSubdomain Template : SubscriptionId : XXXXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df54-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="2df54-116">Crie um aplicativo Central de IoT com o nível de preço padrão ST2 na região "westus", com um nome de exibição personalizado, com base no modelo padrão iotc.</span><span class="sxs-lookup"><span data-stu-id="2df54-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="2df54-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2df54-117">PARAMETERS</span></span>

### <span data-ttu-id="2df54-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2df54-118">-AsJob</span></span>
<span data-ttu-id="2df54-119">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2df54-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="2df54-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df54-120">-DefaultProfile</span></span>
<span data-ttu-id="2df54-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2df54-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2df54-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2df54-122">-DisplayName</span></span>
<span data-ttu-id="2df54-123">Nome de exibição personalizado para o aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="2df54-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="2df54-124">O padrão é o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2df54-124">Default is resource name.</span></span>

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

### <span data-ttu-id="2df54-125">-Local</span><span class="sxs-lookup"><span data-stu-id="2df54-125">-Location</span></span>
<span data-ttu-id="2df54-126">Local do aplicativo Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="2df54-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="2df54-127">O padrão é o local do grupo de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="2df54-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="2df54-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2df54-128">-Name</span></span>
<span data-ttu-id="2df54-129">Nome do Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="2df54-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="2df54-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df54-130">-ResourceGroupName</span></span>
<span data-ttu-id="2df54-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="2df54-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="2df54-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="2df54-132">-Sku</span></span>
<span data-ttu-id="2df54-133">Nível de preço para aplicativos Da Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="2df54-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="2df54-134">O valor padrão é ST2.</span><span class="sxs-lookup"><span data-stu-id="2df54-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="2df54-135">-Subdomínio</span><span class="sxs-lookup"><span data-stu-id="2df54-135">-Subdomain</span></span>
<span data-ttu-id="2df54-136">Subdomínio para a URL Central de IoT.</span><span class="sxs-lookup"><span data-stu-id="2df54-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="2df54-137">Cada aplicativo deve ter um subdomínio exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2df54-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="2df54-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="2df54-138">-Tag</span></span>
<span data-ttu-id="2df54-139">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="2df54-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="2df54-140">-Modelo</span><span class="sxs-lookup"><span data-stu-id="2df54-140">-Template</span></span>
<span data-ttu-id="2df54-141">Nome do modelo de aplicativo central IoT.</span><span class="sxs-lookup"><span data-stu-id="2df54-141">IoT Central application template name.</span></span>
<span data-ttu-id="2df54-142">O padrão é um aplicativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="2df54-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="2df54-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2df54-143">-Confirm</span></span>
<span data-ttu-id="2df54-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2df54-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df54-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df54-145">-WhatIf</span></span>
<span data-ttu-id="2df54-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2df54-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df54-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2df54-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df54-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df54-148">CommonParameters</span></span>
<span data-ttu-id="2df54-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df54-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df54-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2df54-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df54-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="2df54-151">INPUTS</span></span>

### <span data-ttu-id="2df54-152">System.String</span><span class="sxs-lookup"><span data-stu-id="2df54-152">System.String</span></span>

### <span data-ttu-id="2df54-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2df54-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2df54-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="2df54-154">OUTPUTS</span></span>

### <span data-ttu-id="2df54-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="2df54-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="2df54-156">Notas</span><span class="sxs-lookup"><span data-stu-id="2df54-156">NOTES</span></span>

## <span data-ttu-id="2df54-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2df54-157">RELATED LINKS</span></span>
