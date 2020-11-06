---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429787"
---
# <span data-ttu-id="0eba4-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="0eba4-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="0eba4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0eba4-102">SYNOPSIS</span></span>
<span data-ttu-id="0eba4-103">Verifica a disponibilidade do nome ou alias do NameSpace especificado (nome de configuração DR)</span><span class="sxs-lookup"><span data-stu-id="0eba4-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eba4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0eba4-104">SYNTAX</span></span>

### <span data-ttu-id="0eba4-105">NamespaceCheckNameAvailabilitySet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0eba4-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eba4-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0eba4-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eba4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0eba4-107">DESCRIPTION</span></span>
<span data-ttu-id="0eba4-108">O cmdlet **Test-AzureRmEventhubName** verifica a disponibilidade do nome do namespace ou alias (nome de configuração de Dr)</span><span class="sxs-lookup"><span data-stu-id="0eba4-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="0eba4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0eba4-109">EXAMPLES</span></span>

### <span data-ttu-id="0eba4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0eba4-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="0eba4-111">Retorna o status na disponibilidade do nome do namespace ' MyNameSapceName ' como verdadeiro</span><span class="sxs-lookup"><span data-stu-id="0eba4-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="0eba4-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0eba4-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="0eba4-113">Retorna o status de disponibilidade do nome do namespace ' MyNameSapceName ' como falso com motivo</span><span class="sxs-lookup"><span data-stu-id="0eba4-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="0eba4-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0eba4-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="0eba4-115">Retorna o status na disponibilidade do nome do alias ' myaliasname ' no namespace ' MyNameSapceName ' como verdadeiro</span><span class="sxs-lookup"><span data-stu-id="0eba4-115">Returns the status on availability of the alias name 'myAliasName' under namespace 'MyNameSapceName' as True</span></span>

## <span data-ttu-id="0eba4-116">OS</span><span class="sxs-lookup"><span data-stu-id="0eba4-116">PARAMETERS</span></span>

### <span data-ttu-id="0eba4-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="0eba4-117">-AliasName</span></span>
<span data-ttu-id="0eba4-118">Nome de configuração DR-nome do alias</span><span class="sxs-lookup"><span data-stu-id="0eba4-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eba4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eba4-119">-DefaultProfile</span></span>
<span data-ttu-id="0eba4-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0eba4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eba4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0eba4-121">-Namespace</span></span>
<span data-ttu-id="0eba4-122">Nome do namespace do Eventhub</span><span class="sxs-lookup"><span data-stu-id="0eba4-122">Eventhub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eba4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eba4-123">-ResourceGroupName</span></span>
<span data-ttu-id="0eba4-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0eba4-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eba4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eba4-125">CommonParameters</span></span>
<span data-ttu-id="0eba4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eba4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0eba4-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eba4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eba4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0eba4-128">INPUTS</span></span>

### <span data-ttu-id="0eba4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0eba4-129">System.String</span></span>


## <span data-ttu-id="0eba4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0eba4-130">OUTPUTS</span></span>

### <span data-ttu-id="0eba4-131">Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="0eba4-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="0eba4-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0eba4-132">NOTES</span></span>

## <span data-ttu-id="0eba4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0eba4-133">RELATED LINKS</span></span>
