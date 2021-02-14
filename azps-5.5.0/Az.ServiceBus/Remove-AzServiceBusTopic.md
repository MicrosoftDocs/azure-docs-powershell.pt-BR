---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117118"
---
# <span data-ttu-id="cff5d-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="cff5d-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="cff5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cff5d-102">SYNOPSIS</span></span>
<span data-ttu-id="cff5d-103">Remove o tópico do namespace de Barra de Serviços especificado.</span><span class="sxs-lookup"><span data-stu-id="cff5d-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="cff5d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cff5d-104">SYNTAX</span></span>

### <span data-ttu-id="cff5d-105">TopicPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cff5d-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cff5d-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cff5d-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cff5d-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cff5d-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cff5d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cff5d-108">DESCRIPTION</span></span>
<span data-ttu-id="cff5d-109">O cmdlet **Remove-AzServiceBusTopic** remove o tópico do namespace de Barra de Serviços especificado.</span><span class="sxs-lookup"><span data-stu-id="cff5d-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="cff5d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cff5d-110">EXAMPLES</span></span>

### <span data-ttu-id="cff5d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cff5d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="cff5d-112">Remove o tópico `SB-Topic_exampl1` do `SB-Example1` namespace.</span><span class="sxs-lookup"><span data-stu-id="cff5d-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="cff5d-113">Exemplo 2: InputObject - Usando Variável:</span><span class="sxs-lookup"><span data-stu-id="cff5d-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="cff5d-114">Exemplo 3: InputObject - Usando a piping:</span><span class="sxs-lookup"><span data-stu-id="cff5d-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="cff5d-115">Exemplo 4: ResourceId using Variable:</span><span class="sxs-lookup"><span data-stu-id="cff5d-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="cff5d-116">Exemplo 5: ResourceId usando o valor de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="cff5d-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="cff5d-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cff5d-117">PARAMETERS</span></span>

### <span data-ttu-id="cff5d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cff5d-118">-AsJob</span></span>
<span data-ttu-id="cff5d-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cff5d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cff5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff5d-120">-DefaultProfile</span></span>
<span data-ttu-id="cff5d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cff5d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cff5d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cff5d-122">-InputObject</span></span>
<span data-ttu-id="cff5d-123">Objeto de tópico da Barra de Serviços</span><span class="sxs-lookup"><span data-stu-id="cff5d-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="cff5d-124">-Name</span></span>
<span data-ttu-id="cff5d-125">Nome do Tópico</span><span class="sxs-lookup"><span data-stu-id="cff5d-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cff5d-126">-Namespace</span></span>
<span data-ttu-id="cff5d-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="cff5d-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cff5d-128">-PassThru</span></span>
<span data-ttu-id="cff5d-129">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cff5d-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="cff5d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff5d-130">-ResourceGroupName</span></span>
<span data-ttu-id="cff5d-131">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cff5d-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cff5d-132">-ResourceId</span></span>
<span data-ttu-id="cff5d-133">ID do Recurso de Tópico da Barra de Serviços</span><span class="sxs-lookup"><span data-stu-id="cff5d-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5d-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cff5d-134">-Confirm</span></span>
<span data-ttu-id="cff5d-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cff5d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cff5d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cff5d-136">-WhatIf</span></span>
<span data-ttu-id="cff5d-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cff5d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cff5d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cff5d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cff5d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff5d-139">CommonParameters</span></span>
<span data-ttu-id="cff5d-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff5d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff5d-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff5d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff5d-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="cff5d-142">INPUTS</span></span>

### <span data-ttu-id="cff5d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="cff5d-143">System.String</span></span>

### <span data-ttu-id="cff5d-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="cff5d-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="cff5d-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="cff5d-145">OUTPUTS</span></span>

### <span data-ttu-id="cff5d-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cff5d-146">System.Boolean</span></span>

## <span data-ttu-id="cff5d-147">Notas</span><span class="sxs-lookup"><span data-stu-id="cff5d-147">NOTES</span></span>

## <span data-ttu-id="cff5d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cff5d-148">RELATED LINKS</span></span>
