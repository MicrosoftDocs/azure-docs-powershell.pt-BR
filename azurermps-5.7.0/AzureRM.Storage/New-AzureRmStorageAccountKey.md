---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432380"
---
# <span data-ttu-id="ac809-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ac809-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="ac809-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac809-102">SYNOPSIS</span></span>
<span data-ttu-id="ac809-103">Gera novamente uma chave de armazenamento para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ac809-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac809-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac809-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="ac809-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac809-105">DESCRIPTION</span></span>
<span data-ttu-id="ac809-106">O cmdlet **New-AzureRmStorageAccountKey** regenera uma chave de armazenamento para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ac809-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="ac809-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac809-107">EXAMPLES</span></span>

### <span data-ttu-id="ac809-108">Exemplo 1: regenerar uma chave de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ac809-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="ac809-109">Esse comando regenera a chave de armazenamento da conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="ac809-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="ac809-110">OS</span><span class="sxs-lookup"><span data-stu-id="ac809-110">PARAMETERS</span></span>

### <span data-ttu-id="ac809-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ac809-111">-KeyName</span></span>
<span data-ttu-id="ac809-112">Especifica a chave a ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="ac809-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="ac809-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ac809-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac809-114">key1</span><span class="sxs-lookup"><span data-stu-id="ac809-114">key1</span></span>
- <span data-ttu-id="ac809-115">key2</span><span class="sxs-lookup"><span data-stu-id="ac809-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac809-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac809-116">-Name</span></span>
<span data-ttu-id="ac809-117">Especifica o nome da conta de armazenamento para a qual gerar uma chave de armazenamento novamente.</span><span class="sxs-lookup"><span data-stu-id="ac809-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac809-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac809-118">-ResourceGroupName</span></span>
<span data-ttu-id="ac809-119">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ac809-119">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="ac809-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac809-120">CommonParameters</span></span>
<span data-ttu-id="ac809-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac809-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac809-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac809-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac809-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac809-123">INPUTS</span></span>

### <span data-ttu-id="ac809-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ac809-124">None</span></span>
<span data-ttu-id="ac809-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ac809-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac809-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac809-126">OUTPUTS</span></span>

## <span data-ttu-id="ac809-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac809-127">NOTES</span></span>

## <span data-ttu-id="ac809-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac809-128">RELATED LINKS</span></span>

[<span data-ttu-id="ac809-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ac809-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
