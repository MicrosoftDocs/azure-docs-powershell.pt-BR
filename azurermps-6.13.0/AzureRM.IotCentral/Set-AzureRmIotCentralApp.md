---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610896"
---
# <span data-ttu-id="071af-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="071af-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="071af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="071af-102">SYNOPSIS</span></span>
<span data-ttu-id="071af-103">Atualiza os metadados de um aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="071af-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="071af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="071af-104">SYNTAX</span></span>

### <span data-ttu-id="071af-105">ResourceIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="071af-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="071af-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="071af-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="071af-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="071af-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="071af-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="071af-108">DESCRIPTION</span></span>
<span data-ttu-id="071af-109">Atualize os metadados para um aplicativo da central de IoT.</span><span class="sxs-lookup"><span data-stu-id="071af-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="071af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="071af-110">EXAMPLES</span></span>

### <span data-ttu-id="071af-111">Exemplo 1 nome para exibição da atualização</span><span class="sxs-lookup"><span data-stu-id="071af-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="071af-112">Atualize o nome para exibição em um aplicativo Central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="071af-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="071af-113">Exemplo de saída:</span><span class="sxs-lookup"><span data-stu-id="071af-113">Example Output:</span></span>

<span data-ttu-id="071af-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu novo nome de exibição personalizado subdomínio: MyAppSubdomain modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="071af-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="071af-115">OS</span><span class="sxs-lookup"><span data-stu-id="071af-115">PARAMETERS</span></span>

### <span data-ttu-id="071af-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="071af-116">-AsJob</span></span>
<span data-ttu-id="071af-117">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="071af-117">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="071af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="071af-118">-DefaultProfile</span></span>
<span data-ttu-id="071af-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="071af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="071af-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="071af-120">-DisplayName</span></span>
<span data-ttu-id="071af-121">Nome de exibição personalizado do aplicativo da central de IOT.</span><span class="sxs-lookup"><span data-stu-id="071af-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071af-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="071af-122">-InputObject</span></span>
<span data-ttu-id="071af-123">Objeto de entrada de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="071af-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="071af-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="071af-124">-Name</span></span>
<span data-ttu-id="071af-125">Nome do recurso de aplicativo da central do IOT.</span><span class="sxs-lookup"><span data-stu-id="071af-125">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="071af-126">-ResourceGroupName</span></span>
<span data-ttu-id="071af-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="071af-127">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071af-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="071af-128">-ResourceId</span></span>
<span data-ttu-id="071af-129">ID do recurso de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="071af-129">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="071af-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="071af-130">-Tag</span></span>
<span data-ttu-id="071af-131">Marcas de recursos de aplicativo do IOT central.</span><span class="sxs-lookup"><span data-stu-id="071af-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071af-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="071af-132">-Confirm</span></span>
<span data-ttu-id="071af-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="071af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="071af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="071af-134">-WhatIf</span></span>
<span data-ttu-id="071af-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="071af-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="071af-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="071af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="071af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="071af-137">CommonParameters</span></span>
<span data-ttu-id="071af-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="071af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="071af-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="071af-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="071af-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="071af-140">INPUTS</span></span>

### <span data-ttu-id="071af-141">System. String</span><span class="sxs-lookup"><span data-stu-id="071af-141">System.String</span></span>
### <span data-ttu-id="071af-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="071af-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="071af-143">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="071af-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="071af-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="071af-144">OUTPUTS</span></span>

### <span data-ttu-id="071af-145">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="071af-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="071af-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="071af-146">NOTES</span></span>

## <span data-ttu-id="071af-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="071af-147">RELATED LINKS</span></span>
