---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 78fdf68ecb8c50d0eebf4611b51a2fad14c66e5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596307"
---
# <span data-ttu-id="e6fd1-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e6fd1-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="e6fd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fd1-103">Atualiza os metadados de um aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="e6fd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6fd1-104">SYNTAX</span></span>

### <span data-ttu-id="e6fd1-105">ResourceIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6fd1-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6fd1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fd1-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6fd1-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fd1-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6fd1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6fd1-108">DESCRIPTION</span></span>
<span data-ttu-id="e6fd1-109">Atualize os metadados para um aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="e6fd1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6fd1-110">EXAMPLES</span></span>

### <span data-ttu-id="e6fd1-111">Exemplo 1 nome para exibição da atualização</span><span class="sxs-lookup"><span data-stu-id="e6fd1-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="e6fd1-112">Atualize o nome para exibição em um aplicativo Central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="e6fd1-113">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="e6fd1-113">Example Output:</span></span>

<span data-ttu-id="e6fd1-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu novo nome de exibição personalizado subdomínio: MyAppSubdomain modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fd1-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="e6fd1-115">Exemplo 2 subdomínio de atualização</span><span class="sxs-lookup"><span data-stu-id="e6fd1-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="e6fd1-116">Atualize o nome para exibição em um aplicativo Central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="e6fd1-117">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="e6fd1-117">Example Output:</span></span>

<span data-ttu-id="e6fd1-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Templates. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: exibir nome do subdomínio: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName-Display Name: iotc-default@1.0.0 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fd1-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="e6fd1-119">OS</span><span class="sxs-lookup"><span data-stu-id="e6fd1-119">PARAMETERS</span></span>

### <span data-ttu-id="e6fd1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6fd1-120">-AsJob</span></span>
<span data-ttu-id="e6fd1-121">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="e6fd1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fd1-122">-DefaultProfile</span></span>
<span data-ttu-id="e6fd1-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6fd1-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e6fd1-124">-DisplayName</span></span>
<span data-ttu-id="e6fd1-125">Nome de exibição personalizado do aplicativo da central de IOT.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="e6fd1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6fd1-126">-InputObject</span></span>
<span data-ttu-id="e6fd1-127">Objeto de entrada de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="e6fd1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6fd1-128">-Name</span></span>
<span data-ttu-id="e6fd1-129">Nome do recurso de aplicativo da central do IOT.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="e6fd1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fd1-130">-ResourceGroupName</span></span>
<span data-ttu-id="e6fd1-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="e6fd1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6fd1-132">-ResourceId</span></span>
<span data-ttu-id="e6fd1-133">ID do recurso de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="e6fd1-134">-Subdomínio</span><span class="sxs-lookup"><span data-stu-id="e6fd1-134">-Subdomain</span></span>
<span data-ttu-id="e6fd1-135">Subdomínio do aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="e6fd1-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="e6fd1-136">-Tag</span></span>
<span data-ttu-id="e6fd1-137">Marcas de recursos de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="e6fd1-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e6fd1-138">-Confirm</span></span>
<span data-ttu-id="e6fd1-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6fd1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6fd1-140">-WhatIf</span></span>
<span data-ttu-id="e6fd1-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6fd1-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6fd1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fd1-143">CommonParameters</span></span>
<span data-ttu-id="e6fd1-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6fd1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fd1-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6fd1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fd1-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6fd1-146">INPUTS</span></span>

### <span data-ttu-id="e6fd1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e6fd1-147">System.String</span></span>

### <span data-ttu-id="e6fd1-148">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e6fd1-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="e6fd1-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6fd1-149">OUTPUTS</span></span>

### <span data-ttu-id="e6fd1-150">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e6fd1-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="e6fd1-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6fd1-151">NOTES</span></span>

## <span data-ttu-id="e6fd1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6fd1-152">RELATED LINKS</span></span>
