---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 0da9ecf9fabaa1cbb21a5fe8f82bb172b84850e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602532"
---
# <span data-ttu-id="0522a-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="0522a-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="0522a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0522a-102">SYNOPSIS</span></span>
<span data-ttu-id="0522a-103">Invoca o failover de DR geográfico e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="0522a-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0522a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0522a-104">SYNTAX</span></span>

### <span data-ttu-id="0522a-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0522a-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0522a-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0522a-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0522a-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0522a-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0522a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0522a-108">DESCRIPTION</span></span>
<span data-ttu-id="0522a-109">O cmdlet **set-AzureRmEventHubGeoDRConfigurationFailOver** envokes o failover de Dr geográfico e reconfigure o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="0522a-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="0522a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0522a-110">EXAMPLES</span></span>

### <span data-ttu-id="0522a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0522a-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="0522a-112">Invoca o failover por alias "SampleDRCongifName", reconfigura e aponta para o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="0522a-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="0522a-113">OS</span><span class="sxs-lookup"><span data-stu-id="0522a-113">PARAMETERS</span></span>

### <span data-ttu-id="0522a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0522a-114">-DefaultProfile</span></span>
<span data-ttu-id="0522a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0522a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0522a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0522a-116">-InputObject</span></span>
<span data-ttu-id="0522a-117">Objeto de configuração GeoDR do Eventhub</span><span class="sxs-lookup"><span data-stu-id="0522a-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="0522a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0522a-118">-Name</span></span>
<span data-ttu-id="0522a-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="0522a-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="0522a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0522a-120">-Namespace</span></span>
<span data-ttu-id="0522a-121">Nome do namespace-namespace secundário</span><span class="sxs-lookup"><span data-stu-id="0522a-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="0522a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0522a-122">-PassThru</span></span>
<span data-ttu-id="0522a-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0522a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0522a-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0522a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0522a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0522a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0522a-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0522a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0522a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0522a-127">-ResourceId</span></span>
<span data-ttu-id="0522a-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0522a-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="0522a-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0522a-129">-Confirm</span></span>
<span data-ttu-id="0522a-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0522a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0522a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0522a-131">-WhatIf</span></span>
<span data-ttu-id="0522a-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0522a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0522a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0522a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0522a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0522a-134">CommonParameters</span></span>
<span data-ttu-id="0522a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0522a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0522a-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0522a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0522a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0522a-137">INPUTS</span></span>

### <span data-ttu-id="0522a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0522a-138">System.String</span></span>
<span data-ttu-id="0522a-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0522a-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="0522a-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0522a-140">OUTPUTS</span></span>

### <span data-ttu-id="0522a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0522a-141">System.Boolean</span></span>


## <span data-ttu-id="0522a-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0522a-142">NOTES</span></span>

## <span data-ttu-id="0522a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0522a-143">RELATED LINKS</span></span>
