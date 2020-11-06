---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425653"
---
# <span data-ttu-id="195b6-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="195b6-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="195b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="195b6-102">SYNOPSIS</span></span>
<span data-ttu-id="195b6-103">Cria uma política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="195b6-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="195b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="195b6-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="195b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="195b6-105">DESCRIPTION</span></span>
<span data-ttu-id="195b6-106">O cmdlet **New-AzureStorageTableStoredAccessPolicy** cria uma política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="195b6-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="195b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="195b6-107">EXAMPLES</span></span>

### <span data-ttu-id="195b6-108">Exemplo 1: criar uma política de acesso armazenada em uma tabela</span><span class="sxs-lookup"><span data-stu-id="195b6-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="195b6-109">Esse comando cria uma política de acesso chamada Policy02 na tabela armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="195b6-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="195b6-110">OS</span><span class="sxs-lookup"><span data-stu-id="195b6-110">PARAMETERS</span></span>

### <span data-ttu-id="195b6-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="195b6-111">-Context</span></span>
<span data-ttu-id="195b6-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="195b6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="195b6-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="195b6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="195b6-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="195b6-114">-ExpiryTime</span></span>
<span data-ttu-id="195b6-115">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="195b6-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195b6-116">-Permissão</span><span class="sxs-lookup"><span data-stu-id="195b6-116">-Permission</span></span>
<span data-ttu-id="195b6-117">Especifica o nível de acesso público a essa tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="195b6-117">Specifies the level of public access to this storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195b6-118">-Política</span><span class="sxs-lookup"><span data-stu-id="195b6-118">-Policy</span></span>
<span data-ttu-id="195b6-119">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="195b6-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195b6-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="195b6-120">-StartTime</span></span>
<span data-ttu-id="195b6-121">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="195b6-121">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195b6-122">-Tabela</span><span class="sxs-lookup"><span data-stu-id="195b6-122">-Table</span></span>
<span data-ttu-id="195b6-123">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="195b6-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="195b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195b6-124">CommonParameters</span></span>
<span data-ttu-id="195b6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195b6-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195b6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195b6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="195b6-127">INPUTS</span></span>

## <span data-ttu-id="195b6-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="195b6-128">OUTPUTS</span></span>

## <span data-ttu-id="195b6-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="195b6-129">NOTES</span></span>

## <span data-ttu-id="195b6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="195b6-130">RELATED LINKS</span></span>

[<span data-ttu-id="195b6-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="195b6-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="195b6-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="195b6-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="195b6-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="195b6-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="195b6-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="195b6-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


