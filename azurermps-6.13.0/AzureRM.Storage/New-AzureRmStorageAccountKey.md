---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: e44ccbaae730554db35610ff1084e9740e873e53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440712"
---
# <span data-ttu-id="3d844-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3d844-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="3d844-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d844-102">SYNOPSIS</span></span>
<span data-ttu-id="3d844-103">Gera novamente uma chave de armazenamento para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d844-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d844-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d844-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d844-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d844-105">DESCRIPTION</span></span>
<span data-ttu-id="3d844-106">O cmdlet **New-AzureRmStorageAccountKey** regenera uma chave de armazenamento para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d844-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="3d844-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d844-107">EXAMPLES</span></span>

### <span data-ttu-id="3d844-108">Exemplo 1: regenerar uma chave de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3d844-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="3d844-109">Esse comando regenera a chave de armazenamento da conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="3d844-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="3d844-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d844-110">PARAMETERS</span></span>

### <span data-ttu-id="3d844-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d844-111">-DefaultProfile</span></span>
<span data-ttu-id="3d844-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d844-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d844-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3d844-113">-KeyName</span></span>
<span data-ttu-id="3d844-114">Especifica a chave a ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="3d844-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="3d844-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3d844-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d844-116">key1</span><span class="sxs-lookup"><span data-stu-id="3d844-116">key1</span></span>
- <span data-ttu-id="3d844-117">key2</span><span class="sxs-lookup"><span data-stu-id="3d844-117">key2</span></span>

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

### <span data-ttu-id="3d844-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d844-118">-Name</span></span>
<span data-ttu-id="3d844-119">Especifica o nome da conta de armazenamento para a qual gerar uma chave de armazenamento novamente.</span><span class="sxs-lookup"><span data-stu-id="3d844-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="3d844-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d844-120">-ResourceGroupName</span></span>
<span data-ttu-id="3d844-121">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3d844-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="3d844-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d844-122">CommonParameters</span></span>
<span data-ttu-id="3d844-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d844-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d844-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d844-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d844-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d844-125">INPUTS</span></span>

### <span data-ttu-id="3d844-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3d844-126">System.String</span></span>

## <span data-ttu-id="3d844-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d844-127">OUTPUTS</span></span>

### <span data-ttu-id="3d844-128">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3d844-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="3d844-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d844-129">NOTES</span></span>

## <span data-ttu-id="3d844-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d844-130">RELATED LINKS</span></span>

[<span data-ttu-id="3d844-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3d844-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
