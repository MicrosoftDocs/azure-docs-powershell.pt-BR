---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946549"
---
# <span data-ttu-id="225fd-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="225fd-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="225fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="225fd-102">SYNOPSIS</span></span>
<span data-ttu-id="225fd-103">Obtém o contexto de recurso atual.</span><span class="sxs-lookup"><span data-stu-id="225fd-103">Gets the current resource context.</span></span>

## <span data-ttu-id="225fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="225fd-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="225fd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="225fd-105">DESCRIPTION</span></span>
<span data-ttu-id="225fd-106">O cmdlet **Get-AzureStorSimpleResourceContext** Obtém o contexto de recurso atual.</span><span class="sxs-lookup"><span data-stu-id="225fd-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="225fd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="225fd-107">EXAMPLES</span></span>

### <span data-ttu-id="225fd-108">Exemplo 1: obter o contexto atual</span><span class="sxs-lookup"><span data-stu-id="225fd-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="225fd-109">O primeiro comando define o contexto atual para ser o recurso chamado Contoso63-Tsqa usando o cmdlet **Select-AzureStorSimpleResource** .</span><span class="sxs-lookup"><span data-stu-id="225fd-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="225fd-110">O segundo comando obtém o contexto de recurso atual.</span><span class="sxs-lookup"><span data-stu-id="225fd-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="225fd-111">Exemplo 2: tentativa de obter o contexto atual</span><span class="sxs-lookup"><span data-stu-id="225fd-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="225fd-112">Esse comando obtém o contexto atual.</span><span class="sxs-lookup"><span data-stu-id="225fd-112">This command gets the current context.</span></span>
<span data-ttu-id="225fd-113">Neste exemplo, nenhum contexto foi definido.</span><span class="sxs-lookup"><span data-stu-id="225fd-113">In this example, no context has been set.</span></span>
<span data-ttu-id="225fd-114">O comando retorna uma mensagem que explica o problema.</span><span class="sxs-lookup"><span data-stu-id="225fd-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="225fd-115">OS</span><span class="sxs-lookup"><span data-stu-id="225fd-115">PARAMETERS</span></span>

### <span data-ttu-id="225fd-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="225fd-116">-Profile</span></span>
<span data-ttu-id="225fd-117">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="225fd-117">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225fd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225fd-118">CommonParameters</span></span>
<span data-ttu-id="225fd-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225fd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225fd-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225fd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225fd-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="225fd-121">INPUTS</span></span>

### <span data-ttu-id="225fd-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="225fd-122">None</span></span>

## <span data-ttu-id="225fd-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="225fd-123">OUTPUTS</span></span>

### <span data-ttu-id="225fd-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="225fd-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="225fd-125">Esse cmdlet retorna um objeto **ResourceContext** .</span><span class="sxs-lookup"><span data-stu-id="225fd-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="225fd-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="225fd-126">NOTES</span></span>

## <span data-ttu-id="225fd-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="225fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="225fd-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="225fd-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="225fd-129">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="225fd-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


