---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429374"
---
# <span data-ttu-id="28880-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="28880-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="28880-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28880-102">SYNOPSIS</span></span>
<span data-ttu-id="28880-103">Verifica a disponibilidade do nome ou alias do NameSpace especificado (nome de configuração DR)</span><span class="sxs-lookup"><span data-stu-id="28880-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="28880-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28880-104">SYNTAX</span></span>

### <span data-ttu-id="28880-105">NamespaceCheckNameAvailabilitySet (padrão)</span><span class="sxs-lookup"><span data-stu-id="28880-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28880-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="28880-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28880-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28880-107">DESCRIPTION</span></span>
<span data-ttu-id="28880-108">O cmdlet **Test-AzEventhubName** verifica a disponibilidade do nome do namespace ou alias (nome de configuração de Dr)</span><span class="sxs-lookup"><span data-stu-id="28880-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="28880-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28880-109">EXAMPLES</span></span>

### <span data-ttu-id="28880-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28880-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="28880-111">Retorna o status na disponibilidade do nome do namespace ' MyNameSapceName ' como verdadeiro, se disponível</span><span class="sxs-lookup"><span data-stu-id="28880-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="28880-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28880-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="28880-113">Retorna o status de disponibilidade do nome do namespace ' MyNameSapceName ' como falso com motivo</span><span class="sxs-lookup"><span data-stu-id="28880-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="28880-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="28880-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="28880-115">Retorna o status de disponibilidade do nome do alias ' myaliasname ' para o namespace ' MyNameSapceName ' como verdadeiro, se disponível</span><span class="sxs-lookup"><span data-stu-id="28880-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="28880-116">OS</span><span class="sxs-lookup"><span data-stu-id="28880-116">PARAMETERS</span></span>

### <span data-ttu-id="28880-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="28880-117">-AliasName</span></span>
<span data-ttu-id="28880-118">Nome de configuração DR-nome do alias</span><span class="sxs-lookup"><span data-stu-id="28880-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="28880-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28880-119">-DefaultProfile</span></span>
<span data-ttu-id="28880-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28880-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28880-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="28880-121">-Namespace</span></span>
<span data-ttu-id="28880-122">Nome do namespace do Eventhub</span><span class="sxs-lookup"><span data-stu-id="28880-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="28880-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28880-123">-ResourceGroupName</span></span>
<span data-ttu-id="28880-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="28880-124">Resource Group Name</span></span>

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

### <span data-ttu-id="28880-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28880-125">CommonParameters</span></span>
<span data-ttu-id="28880-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28880-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28880-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28880-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28880-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28880-128">INPUTS</span></span>

### <span data-ttu-id="28880-129">System. String</span><span class="sxs-lookup"><span data-stu-id="28880-129">System.String</span></span>

## <span data-ttu-id="28880-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28880-130">OUTPUTS</span></span>

### <span data-ttu-id="28880-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="28880-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="28880-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28880-132">NOTES</span></span>

## <span data-ttu-id="28880-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28880-133">RELATED LINKS</span></span>
