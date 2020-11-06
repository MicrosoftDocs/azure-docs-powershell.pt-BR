---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426138"
---
# <span data-ttu-id="9f416-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9f416-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="9f416-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f416-102">SYNOPSIS</span></span>
<span data-ttu-id="9f416-103">Obtém a política de acesso armazenado ou políticas para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f416-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="9f416-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f416-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f416-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f416-105">DESCRIPTION</span></span>
<span data-ttu-id="9f416-106">O cmdlet **Get-AzureStorageTableStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f416-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="9f416-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f416-107">EXAMPLES</span></span>

### <span data-ttu-id="9f416-108">Exemplo 1: obter uma política de acesso armazenado em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9f416-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="9f416-109">Esse comando obtém a política de acesso chamada Policy50 na tabela armazenamento chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="9f416-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="9f416-110">Exemplo 2: obter todas as políticas de acesso armazenadas em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9f416-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="9f416-111">Esse comando obtém todas as políticas de acesso na tabela chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="9f416-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="9f416-112">OS</span><span class="sxs-lookup"><span data-stu-id="9f416-112">PARAMETERS</span></span>

### <span data-ttu-id="9f416-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9f416-113">-Context</span></span>
<span data-ttu-id="9f416-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f416-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9f416-115">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9f416-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f416-116">-Política</span><span class="sxs-lookup"><span data-stu-id="9f416-116">-Policy</span></span>
<span data-ttu-id="9f416-117">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="9f416-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f416-118">-Tabela</span><span class="sxs-lookup"><span data-stu-id="9f416-118">-Table</span></span>
<span data-ttu-id="9f416-119">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f416-119">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f416-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f416-120">CommonParameters</span></span>
<span data-ttu-id="9f416-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f416-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f416-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f416-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f416-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f416-123">INPUTS</span></span>

## <span data-ttu-id="9f416-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f416-124">OUTPUTS</span></span>

## <span data-ttu-id="9f416-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f416-125">NOTES</span></span>

## <span data-ttu-id="9f416-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f416-126">RELATED LINKS</span></span>

[<span data-ttu-id="9f416-127">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9f416-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="9f416-128">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9f416-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="9f416-129">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9f416-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="9f416-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9f416-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


