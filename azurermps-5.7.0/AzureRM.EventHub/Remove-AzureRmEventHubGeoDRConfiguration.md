---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 929ebdfb9cc38d5233027da75752f4c82c484536
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430493"
---
# <span data-ttu-id="e2d0b-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d0b-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="e2d0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d0b-103">Exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="e2d0b-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2d0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2d0b-104">SYNTAX</span></span>

### <span data-ttu-id="e2d0b-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2d0b-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2d0b-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2d0b-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2d0b-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2d0b-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d0b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2d0b-108">DESCRIPTION</span></span>
<span data-ttu-id="e2d0b-109">O cmdlet **Remove-AzureRmEventHubGeoDRConfiguration** exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="e2d0b-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="e2d0b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2d0b-110">EXAMPLES</span></span>

### <span data-ttu-id="e2d0b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2d0b-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="e2d0b-112">Exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="e2d0b-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="e2d0b-113">OS</span><span class="sxs-lookup"><span data-stu-id="e2d0b-113">PARAMETERS</span></span>

### <span data-ttu-id="e2d0b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2d0b-114">-AsJob</span></span>
<span data-ttu-id="e2d0b-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e2d0b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2d0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d0b-116">-DefaultProfile</span></span>
<span data-ttu-id="e2d0b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2d0b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2d0b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2d0b-118">-InputObject</span></span>
<span data-ttu-id="e2d0b-119">Objeto de configuração GeoDR do Eventhub</span><span class="sxs-lookup"><span data-stu-id="e2d0b-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d0b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2d0b-120">-Name</span></span>
<span data-ttu-id="e2d0b-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="e2d0b-121">Alias (GeoDR)</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d0b-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2d0b-122">-Namespace</span></span>
<span data-ttu-id="e2d0b-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="e2d0b-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d0b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2d0b-124">-PassThru</span></span>
<span data-ttu-id="e2d0b-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e2d0b-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e2d0b-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e2d0b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e2d0b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d0b-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2d0b-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e2d0b-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d0b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2d0b-129">-ResourceId</span></span>
<span data-ttu-id="e2d0b-130">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d0b-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d0b-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2d0b-131">-Confirm</span></span>
<span data-ttu-id="e2d0b-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2d0b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d0b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d0b-133">-WhatIf</span></span>
<span data-ttu-id="e2d0b-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2d0b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d0b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2d0b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d0b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d0b-136">CommonParameters</span></span>
<span data-ttu-id="e2d0b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d0b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e2d0b-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d0b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d0b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2d0b-139">INPUTS</span></span>

### <span data-ttu-id="e2d0b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e2d0b-140">System.String</span></span>
<span data-ttu-id="e2d0b-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e2d0b-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="e2d0b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2d0b-142">OUTPUTS</span></span>

### <span data-ttu-id="e2d0b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2d0b-143">System.Boolean</span></span>


## <span data-ttu-id="e2d0b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2d0b-144">NOTES</span></span>

## <span data-ttu-id="e2d0b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2d0b-145">RELATED LINKS</span></span>
