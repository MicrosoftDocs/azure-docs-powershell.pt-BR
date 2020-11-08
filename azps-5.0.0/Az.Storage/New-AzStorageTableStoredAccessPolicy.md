---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 82e5d252e2e8185b98c142b24537c666e5618d7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125281"
---
# <span data-ttu-id="7ce6e-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce6e-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="7ce6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ce6e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce6e-103">Cria uma política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="7ce6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ce6e-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ce6e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ce6e-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce6e-106">O cmdlet **New-AzStorageTableStoredAccessPolicy** cria uma política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="7ce6e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ce6e-107">EXAMPLES</span></span>

### <span data-ttu-id="7ce6e-108">Exemplo 1: criar uma política de acesso armazenada em uma tabela</span><span class="sxs-lookup"><span data-stu-id="7ce6e-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="7ce6e-109">Esse comando cria uma política de acesso chamada Policy02 na tabela armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="7ce6e-110">OS</span><span class="sxs-lookup"><span data-stu-id="7ce6e-110">PARAMETERS</span></span>

### <span data-ttu-id="7ce6e-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7ce6e-111">-Context</span></span>
<span data-ttu-id="7ce6e-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7ce6e-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7ce6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce6e-114">-DefaultProfile</span></span>
<span data-ttu-id="7ce6e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce6e-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7ce6e-116">-ExpiryTime</span></span>
<span data-ttu-id="7ce6e-117">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6e-118">-Permissão</span><span class="sxs-lookup"><span data-stu-id="7ce6e-118">-Permission</span></span>
<span data-ttu-id="7ce6e-119">Especifica as permissões na política de acesso armazenado para acessar a tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="7ce6e-120">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="7ce6e-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6e-121">-Política</span><span class="sxs-lookup"><span data-stu-id="7ce6e-121">-Policy</span></span>
<span data-ttu-id="7ce6e-122">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6e-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7ce6e-123">-StartTime</span></span>
<span data-ttu-id="7ce6e-124">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce6e-125">-Tabela</span><span class="sxs-lookup"><span data-stu-id="7ce6e-125">-Table</span></span>
<span data-ttu-id="7ce6e-126">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="7ce6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce6e-127">CommonParameters</span></span>
<span data-ttu-id="7ce6e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce6e-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce6e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce6e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ce6e-130">INPUTS</span></span>

### <span data-ttu-id="7ce6e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7ce6e-131">System.String</span></span>

### <span data-ttu-id="7ce6e-132">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ce6e-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7ce6e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ce6e-133">OUTPUTS</span></span>

### <span data-ttu-id="7ce6e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7ce6e-134">System.String</span></span>

## <span data-ttu-id="7ce6e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ce6e-135">NOTES</span></span>

## <span data-ttu-id="7ce6e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ce6e-136">RELATED LINKS</span></span>

[<span data-ttu-id="7ce6e-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce6e-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7ce6e-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ce6e-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7ce6e-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce6e-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7ce6e-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce6e-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


