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
ms.locfileid: "93770748"
---
# <span data-ttu-id="ce7c9-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ce7c9-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="ce7c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7c9-103">Atualiza os metadados de um aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="ce7c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce7c9-104">SYNTAX</span></span>

### <span data-ttu-id="ce7c9-105">ResourceIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce7c9-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7c9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce7c9-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce7c9-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce7c9-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce7c9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce7c9-108">DESCRIPTION</span></span>
<span data-ttu-id="ce7c9-109">Atualize os metadados para um aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="ce7c9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce7c9-110">EXAMPLES</span></span>

### <span data-ttu-id="ce7c9-111">Exemplo 1 nome para exibição da atualização</span><span class="sxs-lookup"><span data-stu-id="ce7c9-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="ce7c9-112">Atualize o nome para exibição em um aplicativo Central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="ce7c9-113">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="ce7c9-113">Example Output:</span></span>

<span data-ttu-id="ce7c9-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu novo nome de exibição personalizado subdomínio: MyAppSubdomain modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7c9-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="ce7c9-115">Exemplo 2 subdomínio de atualização</span><span class="sxs-lookup"><span data-stu-id="ce7c9-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="ce7c9-116">Atualize o nome para exibição em um aplicativo Central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="ce7c9-117">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="ce7c9-117">Example Output:</span></span>

<span data-ttu-id="ce7c9-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Templates. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: exibir nome do subdomínio: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName-Display Name: iotc-default@1.0.0 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7c9-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="ce7c9-119">OS</span><span class="sxs-lookup"><span data-stu-id="ce7c9-119">PARAMETERS</span></span>

### <span data-ttu-id="ce7c9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce7c9-120">-AsJob</span></span>
<span data-ttu-id="ce7c9-121">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="ce7c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7c9-122">-DefaultProfile</span></span>
<span data-ttu-id="ce7c9-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce7c9-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ce7c9-124">-DisplayName</span></span>
<span data-ttu-id="ce7c9-125">Nome de exibição personalizado do aplicativo da central de IOT.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="ce7c9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce7c9-126">-InputObject</span></span>
<span data-ttu-id="ce7c9-127">Objeto de entrada de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="ce7c9-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce7c9-128">-Name</span></span>
<span data-ttu-id="ce7c9-129">Nome do recurso de aplicativo da central do IOT.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="ce7c9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7c9-130">-ResourceGroupName</span></span>
<span data-ttu-id="ce7c9-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="ce7c9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce7c9-132">-ResourceId</span></span>
<span data-ttu-id="ce7c9-133">ID do recurso de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="ce7c9-134">-Subdomínio</span><span class="sxs-lookup"><span data-stu-id="ce7c9-134">-Subdomain</span></span>
<span data-ttu-id="ce7c9-135">Subdomínio do aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="ce7c9-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="ce7c9-136">-Tag</span></span>
<span data-ttu-id="ce7c9-137">Marcas de recursos de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="ce7c9-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce7c9-138">-Confirm</span></span>
<span data-ttu-id="ce7c9-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce7c9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce7c9-140">-WhatIf</span></span>
<span data-ttu-id="ce7c9-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce7c9-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce7c9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7c9-143">CommonParameters</span></span>
<span data-ttu-id="ce7c9-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7c9-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce7c9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7c9-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce7c9-146">INPUTS</span></span>

### <span data-ttu-id="ce7c9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ce7c9-147">System.String</span></span>

### <span data-ttu-id="ce7c9-148">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ce7c9-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="ce7c9-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce7c9-149">OUTPUTS</span></span>

### <span data-ttu-id="ce7c9-150">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ce7c9-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="ce7c9-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce7c9-151">NOTES</span></span>

## <span data-ttu-id="ce7c9-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce7c9-152">RELATED LINKS</span></span>
