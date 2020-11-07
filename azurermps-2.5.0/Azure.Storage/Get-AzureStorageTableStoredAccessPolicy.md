---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a9c141684eb924ed0b969c469214d92b847e13db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786026"
---
# <span data-ttu-id="54620-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="54620-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="54620-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54620-102">SYNOPSIS</span></span>
<span data-ttu-id="54620-103">Obtém a política de acesso armazenado ou políticas para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="54620-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54620-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54620-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54620-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54620-105">DESCRIPTION</span></span>
<span data-ttu-id="54620-106">O cmdlet **Get-AzureStorageTableStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="54620-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="54620-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54620-107">EXAMPLES</span></span>

### <span data-ttu-id="54620-108">Exemplo 1: obter uma política de acesso armazenado em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="54620-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="54620-109">Esse comando obtém a política de acesso chamada Policy50 na tabela armazenamento chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="54620-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="54620-110">Exemplo 2: obter todas as políticas de acesso armazenadas em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="54620-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="54620-111">Esse comando obtém todas as políticas de acesso na tabela chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="54620-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="54620-112">OS</span><span class="sxs-lookup"><span data-stu-id="54620-112">PARAMETERS</span></span>

### <span data-ttu-id="54620-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="54620-113">-Context</span></span>
<span data-ttu-id="54620-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="54620-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="54620-115">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="54620-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="54620-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54620-116">-DefaultProfile</span></span>
<span data-ttu-id="54620-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54620-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54620-118">-Política</span><span class="sxs-lookup"><span data-stu-id="54620-118">-Policy</span></span>
<span data-ttu-id="54620-119">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="54620-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="54620-120">-Tabela</span><span class="sxs-lookup"><span data-stu-id="54620-120">-Table</span></span>
<span data-ttu-id="54620-121">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="54620-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="54620-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54620-122">CommonParameters</span></span>
<span data-ttu-id="54620-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54620-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54620-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54620-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54620-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54620-125">INPUTS</span></span>

### <span data-ttu-id="54620-126">System. String</span><span class="sxs-lookup"><span data-stu-id="54620-126">System.String</span></span>

### <span data-ttu-id="54620-127">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="54620-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="54620-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54620-128">OUTPUTS</span></span>

### <span data-ttu-id="54620-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="54620-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="54620-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54620-130">NOTES</span></span>

## <span data-ttu-id="54620-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54620-131">RELATED LINKS</span></span>

[<span data-ttu-id="54620-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="54620-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="54620-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="54620-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="54620-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="54620-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="54620-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="54620-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


