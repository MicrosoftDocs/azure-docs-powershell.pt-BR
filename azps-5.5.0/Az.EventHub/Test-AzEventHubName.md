---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117654"
---
# <span data-ttu-id="8b356-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="8b356-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="8b356-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b356-102">SYNOPSIS</span></span>
<span data-ttu-id="8b356-103">Verifica a Disponibilidade do nome namespace ou alias (nome de configuração dr) determinado</span><span class="sxs-lookup"><span data-stu-id="8b356-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="8b356-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b356-104">SYNTAX</span></span>

### <span data-ttu-id="8b356-105">NamespaceCheckNameAvailabilitySet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8b356-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b356-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8b356-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b356-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b356-107">DESCRIPTION</span></span>
<span data-ttu-id="8b356-108">O **cmdlet Test-AzEventhubName Disponibilidade** do nome namespace ou alias (nome de configuração dr)</span><span class="sxs-lookup"><span data-stu-id="8b356-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="8b356-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b356-109">EXAMPLES</span></span>

### <span data-ttu-id="8b356-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8b356-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="8b356-111">Retorna o status sobre a disponibilidade do nome do namespace 'MyNameSapceName' como True, se disponível</span><span class="sxs-lookup"><span data-stu-id="8b356-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="8b356-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8b356-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="8b356-113">Retorna o status sobre a disponibilidade do nome do namespace 'MyNameSapceName' como False with Reason</span><span class="sxs-lookup"><span data-stu-id="8b356-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="8b356-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8b356-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="8b356-115">Retorna o status sobre a disponibilidade do nome de alias 'meuAliasName' para namespace 'MyNameSapceName' como True, se disponível</span><span class="sxs-lookup"><span data-stu-id="8b356-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="8b356-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b356-116">PARAMETERS</span></span>

### <span data-ttu-id="8b356-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="8b356-117">-AliasName</span></span>
<span data-ttu-id="8b356-118">Nome de configuração dr – nome de alias</span><span class="sxs-lookup"><span data-stu-id="8b356-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b356-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b356-119">-DefaultProfile</span></span>
<span data-ttu-id="8b356-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b356-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b356-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8b356-121">-Namespace</span></span>
<span data-ttu-id="8b356-122">Nome do Namespace do Eventhub</span><span class="sxs-lookup"><span data-stu-id="8b356-122">Eventhub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b356-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b356-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b356-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8b356-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b356-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b356-125">CommonParameters</span></span>
<span data-ttu-id="8b356-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b356-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b356-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b356-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b356-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="8b356-128">INPUTS</span></span>

### <span data-ttu-id="8b356-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8b356-129">System.String</span></span>

## <span data-ttu-id="8b356-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="8b356-130">OUTPUTS</span></span>

### <span data-ttu-id="8b356-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="8b356-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="8b356-132">Notas</span><span class="sxs-lookup"><span data-stu-id="8b356-132">NOTES</span></span>

## <span data-ttu-id="8b356-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b356-133">RELATED LINKS</span></span>
