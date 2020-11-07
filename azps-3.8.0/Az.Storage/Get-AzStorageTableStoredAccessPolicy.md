---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942277"
---
# <span data-ttu-id="3fc38-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3fc38-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3fc38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fc38-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc38-103">Obtém a política de acesso armazenado ou políticas para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc38-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="3fc38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fc38-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fc38-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fc38-105">DESCRIPTION</span></span>
<span data-ttu-id="3fc38-106">O cmdlet **Get-AzStorageTableStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc38-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="3fc38-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fc38-107">EXAMPLES</span></span>

### <span data-ttu-id="3fc38-108">Exemplo 1: obter uma política de acesso armazenado em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3fc38-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="3fc38-109">Esse comando obtém a política de acesso chamada Policy50 na tabela armazenamento chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="3fc38-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="3fc38-110">Exemplo 2: obter todas as políticas de acesso armazenadas em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3fc38-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="3fc38-111">Esse comando obtém todas as políticas de acesso na tabela chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="3fc38-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="3fc38-112">OS</span><span class="sxs-lookup"><span data-stu-id="3fc38-112">PARAMETERS</span></span>

### <span data-ttu-id="3fc38-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3fc38-113">-Context</span></span>
<span data-ttu-id="3fc38-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc38-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3fc38-115">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3fc38-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc38-116">-DefaultProfile</span></span>
<span data-ttu-id="3fc38-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-118">-Política</span><span class="sxs-lookup"><span data-stu-id="3fc38-118">-Policy</span></span>
<span data-ttu-id="3fc38-119">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="3fc38-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-120">-Tabela</span><span class="sxs-lookup"><span data-stu-id="3fc38-120">-Table</span></span>
<span data-ttu-id="3fc38-121">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc38-121">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc38-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc38-122">CommonParameters</span></span>
<span data-ttu-id="3fc38-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc38-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc38-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc38-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc38-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fc38-125">INPUTS</span></span>

### <span data-ttu-id="3fc38-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3fc38-126">System.String</span></span>

### <span data-ttu-id="3fc38-127">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3fc38-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3fc38-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fc38-128">OUTPUTS</span></span>

### <span data-ttu-id="3fc38-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="3fc38-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="3fc38-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fc38-130">NOTES</span></span>

## <span data-ttu-id="3fc38-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fc38-131">RELATED LINKS</span></span>

[<span data-ttu-id="3fc38-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3fc38-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3fc38-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3fc38-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3fc38-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3fc38-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3fc38-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3fc38-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


