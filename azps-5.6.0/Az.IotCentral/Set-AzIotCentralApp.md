---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: f99faf1ce7420212e87c894c8f5aadeb16578334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891374"
---
# <span data-ttu-id="1a139-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="1a139-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="1a139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a139-102">SYNOPSIS</span></span>
<span data-ttu-id="1a139-103">Atualiza os metadados de um aplicativo central de IoT.</span><span class="sxs-lookup"><span data-stu-id="1a139-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="1a139-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1a139-104">SYNTAX</span></span>

### <span data-ttu-id="1a139-105">ResourceIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1a139-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a139-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a139-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a139-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a139-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a139-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1a139-108">DESCRIPTION</span></span>
<span data-ttu-id="1a139-109">Atualize os metadados para um aplicativo central de IoT.</span><span class="sxs-lookup"><span data-stu-id="1a139-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="1a139-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a139-110">EXAMPLES</span></span>

### <span data-ttu-id="1a139-111">Exemplo 1 Atualizar Nome de Exibição</span><span class="sxs-lookup"><span data-stu-id="1a139-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="1a139-112">Atualize o nome de exibição em um aplicativo central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="1a139-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="1a139-113">Saída de Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1a139-113">Example Output:</span></span>

<span data-ttu-id="1a139-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Nome : MyAppResourceName Tipo : Microsoft.IoTCentral/IoTApps Localização : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppS ApplicationId dekuInfo : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Meu Novo Subdomínio de Nome de Exibição Personalizado : MyAppSubdomain Modelo : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a139-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="1a139-115">Exemplo 2 Update Subdomínio</span><span class="sxs-lookup"><span data-stu-id="1a139-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="1a139-116">Atualize o nome de exibição em um aplicativo central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="1a139-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="1a139-117">Saída de Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1a139-117">Example Output:</span></span>

<span data-ttu-id="1a139-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Nome : MyAppResourceName Tipo : Microsoft.IoTCentral/IoTApps Localização : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Display Name Subdomain : new-subdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a139-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="1a139-119">Exemplo 3 Atualizar Informações do Aplicativo Sku</span><span class="sxs-lookup"><span data-stu-id="1a139-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="1a139-120">Atualize o sku em um Aplicativo Central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="1a139-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="1a139-121">Saída de Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1a139-121">Example Output:</span></span>

<span data-ttu-id="1a139-122">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Nome : MyAppResourceName Tipo : Microsoft.IoTCentral/IoTApps Localização : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp ApplicationId de SkuInfo : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a139-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="1a139-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1a139-123">PARAMETERS</span></span>

### <span data-ttu-id="1a139-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a139-124">-AsJob</span></span>
<span data-ttu-id="1a139-125">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1a139-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="1a139-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a139-126">-DefaultProfile</span></span>
<span data-ttu-id="1a139-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a139-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a139-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1a139-128">-DisplayName</span></span>
<span data-ttu-id="1a139-129">Nome de exibição personalizado do aplicativo central de Iot.</span><span class="sxs-lookup"><span data-stu-id="1a139-129">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a139-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a139-130">-InputObject</span></span>
<span data-ttu-id="1a139-131">Objeto de entrada de aplicativo central Iot.</span><span class="sxs-lookup"><span data-stu-id="1a139-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a139-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1a139-132">-Name</span></span>
<span data-ttu-id="1a139-133">Nome do Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="1a139-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="1a139-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a139-134">-ResourceGroupName</span></span>
<span data-ttu-id="1a139-135">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="1a139-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="1a139-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a139-136">-ResourceId</span></span>
<span data-ttu-id="1a139-137">Id de Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="1a139-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="1a139-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="1a139-138">-Sku</span></span>
<span data-ttu-id="1a139-139">Camada de preços para aplicativos IoT Central.</span><span class="sxs-lookup"><span data-stu-id="1a139-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="1a139-140">O valor padrão é ST2.</span><span class="sxs-lookup"><span data-stu-id="1a139-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="1a139-141">-Subdomínio</span><span class="sxs-lookup"><span data-stu-id="1a139-141">-Subdomain</span></span>
<span data-ttu-id="1a139-142">Subdomínio do Aplicativo Central da IoT.</span><span class="sxs-lookup"><span data-stu-id="1a139-142">Subdomain of the IoT Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a139-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="1a139-143">-Tag</span></span>
<span data-ttu-id="1a139-144">Iot Marcas de Recurso de Aplicativo Central.</span><span class="sxs-lookup"><span data-stu-id="1a139-144">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a139-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a139-145">-Confirm</span></span>
<span data-ttu-id="1a139-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a139-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a139-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a139-147">-WhatIf</span></span>
<span data-ttu-id="1a139-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a139-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a139-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a139-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a139-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a139-150">CommonParameters</span></span>
<span data-ttu-id="1a139-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a139-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a139-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a139-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a139-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a139-153">INPUTS</span></span>

### <span data-ttu-id="1a139-154">System.String</span><span class="sxs-lookup"><span data-stu-id="1a139-154">System.String</span></span>

### <span data-ttu-id="1a139-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="1a139-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="1a139-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1a139-156">OUTPUTS</span></span>

### <span data-ttu-id="1a139-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="1a139-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="1a139-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="1a139-158">NOTES</span></span>

## <span data-ttu-id="1a139-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a139-159">RELATED LINKS</span></span>
