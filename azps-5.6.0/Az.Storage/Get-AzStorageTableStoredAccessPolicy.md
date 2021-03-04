---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 2de23408aef9d9af4ebd23eb520261760883cf3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890920"
---
# <span data-ttu-id="d85e5-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d85e5-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="d85e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d85e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d85e5-103">Obtém a política ou políticas de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d85e5-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="d85e5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d85e5-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d85e5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d85e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d85e5-106">O cmdlet **Get-AzStorageTableStoredAccessPolicy** lista a política de acesso armazenado ou as políticas de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d85e5-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="d85e5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d85e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d85e5-108">Exemplo 1: obter uma política de acesso armazenado em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d85e5-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="d85e5-109">Este comando obtém a política de acesso chamada Policy50 na tabela de armazenamento chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="d85e5-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="d85e5-110">Exemplo 2: Obter todas as políticas de acesso armazenadas em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d85e5-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="d85e5-111">Este comando obtém todas as políticas de acesso na tabela chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="d85e5-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="d85e5-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d85e5-112">PARAMETERS</span></span>

### <span data-ttu-id="d85e5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d85e5-113">-Context</span></span>
<span data-ttu-id="d85e5-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d85e5-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d85e5-115">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d85e5-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d85e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85e5-116">-DefaultProfile</span></span>
<span data-ttu-id="d85e5-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d85e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d85e5-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="d85e5-118">-Policy</span></span>
<span data-ttu-id="d85e5-119">Especifica uma política de acesso armazenada, que inclui as permissões para este token SAS (Assinatura de Acesso Compartilhado).</span><span class="sxs-lookup"><span data-stu-id="d85e5-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="d85e5-120">-Table</span><span class="sxs-lookup"><span data-stu-id="d85e5-120">-Table</span></span>
<span data-ttu-id="d85e5-121">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d85e5-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="d85e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85e5-122">CommonParameters</span></span>
<span data-ttu-id="d85e5-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85e5-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d85e5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85e5-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d85e5-125">INPUTS</span></span>

### <span data-ttu-id="d85e5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d85e5-126">System.String</span></span>

### <span data-ttu-id="d85e5-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d85e5-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d85e5-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d85e5-128">OUTPUTS</span></span>

### <span data-ttu-id="d85e5-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="d85e5-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="d85e5-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="d85e5-130">NOTES</span></span>

## <span data-ttu-id="d85e5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d85e5-131">RELATED LINKS</span></span>

[<span data-ttu-id="d85e5-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d85e5-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d85e5-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d85e5-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d85e5-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d85e5-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d85e5-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d85e5-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


