---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 558452481ed3feef979b78d7f134869d141caa20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596244"
---
# <span data-ttu-id="75626-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="75626-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="75626-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75626-102">SYNOPSIS</span></span>
<span data-ttu-id="75626-103">Exclua uma mensagem aprimorada no seu hub IoT.</span><span class="sxs-lookup"><span data-stu-id="75626-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="75626-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75626-104">SYNTAX</span></span>

### <span data-ttu-id="75626-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75626-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75626-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="75626-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75626-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="75626-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75626-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75626-108">DESCRIPTION</span></span>
<span data-ttu-id="75626-109">Para obter uma explicação detalhada dos aprimoramentos de mensagens no Hub IoT do Azure, consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="75626-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="75626-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75626-110">EXAMPLES</span></span>

### <span data-ttu-id="75626-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75626-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="75626-112">Exclui o "newKey" encompletar mensagem.</span><span class="sxs-lookup"><span data-stu-id="75626-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="75626-113">OS</span><span class="sxs-lookup"><span data-stu-id="75626-113">PARAMETERS</span></span>

### <span data-ttu-id="75626-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75626-114">-DefaultProfile</span></span>
<span data-ttu-id="75626-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75626-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75626-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75626-116">-InputObject</span></span>
<span data-ttu-id="75626-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="75626-117">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75626-118">-Chave</span><span class="sxs-lookup"><span data-stu-id="75626-118">-Key</span></span>
<span data-ttu-id="75626-119">A chave do encompletamento.</span><span class="sxs-lookup"><span data-stu-id="75626-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="75626-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="75626-120">-Name</span></span>
<span data-ttu-id="75626-121">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="75626-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75626-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75626-122">-PassThru</span></span>
<span data-ttu-id="75626-123">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="75626-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="75626-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="75626-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="75626-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75626-125">-ResourceGroupName</span></span>
<span data-ttu-id="75626-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="75626-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75626-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75626-127">-ResourceId</span></span>
<span data-ttu-id="75626-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="75626-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75626-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75626-129">-Confirm</span></span>
<span data-ttu-id="75626-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75626-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75626-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75626-131">-WhatIf</span></span>
<span data-ttu-id="75626-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75626-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75626-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75626-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75626-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75626-134">CommonParameters</span></span>
<span data-ttu-id="75626-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75626-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75626-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75626-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75626-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75626-137">INPUTS</span></span>

### <span data-ttu-id="75626-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="75626-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="75626-139">System. String</span><span class="sxs-lookup"><span data-stu-id="75626-139">System.String</span></span>

## <span data-ttu-id="75626-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75626-140">OUTPUTS</span></span>

### <span data-ttu-id="75626-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75626-141">System.Boolean</span></span>

## <span data-ttu-id="75626-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75626-142">NOTES</span></span>

## <span data-ttu-id="75626-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75626-143">RELATED LINKS</span></span>
