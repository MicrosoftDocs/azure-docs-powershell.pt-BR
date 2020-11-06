---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: 64a8282cb1dc99b32e0296ebf97f59ab96b5fd96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426347"
---
# <span data-ttu-id="d025f-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="d025f-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="d025f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d025f-102">SYNOPSIS</span></span>
<span data-ttu-id="d025f-103">Verifica a disponibilidade do nome ou alias do NameSpace especificado (nome de configuração DR)</span><span class="sxs-lookup"><span data-stu-id="d025f-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d025f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d025f-104">SYNTAX</span></span>

### <span data-ttu-id="d025f-105">NamespaceCheckNameAvailabilitySet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d025f-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d025f-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d025f-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d025f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d025f-107">DESCRIPTION</span></span>
<span data-ttu-id="d025f-108">O cmdlet **Test-AzureRmEventhubName** verifica a disponibilidade do nome do namespace ou alias (nome de configuração de Dr)</span><span class="sxs-lookup"><span data-stu-id="d025f-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="d025f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d025f-109">EXAMPLES</span></span>

### <span data-ttu-id="d025f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d025f-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="d025f-111">Retorna o status na disponibilidade do nome do namespace ' MyNameSapceName ' como verdadeiro, se disponível</span><span class="sxs-lookup"><span data-stu-id="d025f-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="d025f-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d025f-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="d025f-113">Retorna o status de disponibilidade do nome do namespace ' MyNameSapceName ' como falso com motivo</span><span class="sxs-lookup"><span data-stu-id="d025f-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="d025f-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d025f-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="d025f-115">Retorna o status de disponibilidade do nome do alias ' myaliasname ' para o namespace ' MyNameSapceName ' como verdadeiro, se disponível</span><span class="sxs-lookup"><span data-stu-id="d025f-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="d025f-116">OS</span><span class="sxs-lookup"><span data-stu-id="d025f-116">PARAMETERS</span></span>

### <span data-ttu-id="d025f-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="d025f-117">-AliasName</span></span>
<span data-ttu-id="d025f-118">Nome de configuração DR-nome do alias</span><span class="sxs-lookup"><span data-stu-id="d025f-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="d025f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d025f-119">-DefaultProfile</span></span>
<span data-ttu-id="d025f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d025f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025f-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d025f-121">-Namespace</span></span>
<span data-ttu-id="d025f-122">Nome do namespace do Eventhub</span><span class="sxs-lookup"><span data-stu-id="d025f-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="d025f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d025f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d025f-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d025f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d025f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d025f-125">CommonParameters</span></span>
<span data-ttu-id="d025f-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d025f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d025f-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d025f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d025f-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d025f-128">INPUTS</span></span>

### <span data-ttu-id="d025f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d025f-129">System.String</span></span>

## <span data-ttu-id="d025f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d025f-130">OUTPUTS</span></span>

### <span data-ttu-id="d025f-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="d025f-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="d025f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d025f-132">NOTES</span></span>

## <span data-ttu-id="d025f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d025f-133">RELATED LINKS</span></span>
