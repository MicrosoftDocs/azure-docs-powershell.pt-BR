---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: d63c948e59dbc05122c63b6688277a7015a42163
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943145"
---
# <span data-ttu-id="64149-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="64149-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="64149-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64149-102">SYNOPSIS</span></span>
<span data-ttu-id="64149-103">Gera novamente uma chave de armazenamento para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="64149-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="64149-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64149-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64149-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64149-105">DESCRIPTION</span></span>
<span data-ttu-id="64149-106">O cmdlet **New-AzStorageAccountKey** regenera uma chave de armazenamento para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="64149-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="64149-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64149-107">EXAMPLES</span></span>

### <span data-ttu-id="64149-108">Exemplo 1: regenerar uma chave de armazenamento</span><span class="sxs-lookup"><span data-stu-id="64149-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="64149-109">Esse comando regenera a chave de armazenamento da conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="64149-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="64149-110">OS</span><span class="sxs-lookup"><span data-stu-id="64149-110">PARAMETERS</span></span>

### <span data-ttu-id="64149-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64149-111">-DefaultProfile</span></span>
<span data-ttu-id="64149-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64149-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64149-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="64149-113">-KeyName</span></span>
<span data-ttu-id="64149-114">Especifica a chave a ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="64149-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="64149-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="64149-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64149-116">key1</span><span class="sxs-lookup"><span data-stu-id="64149-116">key1</span></span>
- <span data-ttu-id="64149-117">key2</span><span class="sxs-lookup"><span data-stu-id="64149-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64149-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="64149-118">-Name</span></span>
<span data-ttu-id="64149-119">Especifica o nome da conta de armazenamento para a qual gerar uma chave de armazenamento novamente.</span><span class="sxs-lookup"><span data-stu-id="64149-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64149-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64149-120">-ResourceGroupName</span></span>
<span data-ttu-id="64149-121">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="64149-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="64149-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64149-122">CommonParameters</span></span>
<span data-ttu-id="64149-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64149-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64149-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64149-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64149-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64149-125">INPUTS</span></span>

### <span data-ttu-id="64149-126">System. String</span><span class="sxs-lookup"><span data-stu-id="64149-126">System.String</span></span>

## <span data-ttu-id="64149-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64149-127">OUTPUTS</span></span>

### <span data-ttu-id="64149-128">Microsoft. Azure. Management. Storage. Models. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="64149-128">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="64149-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64149-129">NOTES</span></span>

## <span data-ttu-id="64149-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64149-130">RELATED LINKS</span></span>

[<span data-ttu-id="64149-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="64149-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
