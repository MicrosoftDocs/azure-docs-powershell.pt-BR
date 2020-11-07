---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786356"
---
# <span data-ttu-id="fa16e-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa16e-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="fa16e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa16e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa16e-103">Cria uma política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa16e-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa16e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa16e-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa16e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa16e-105">DESCRIPTION</span></span>
<span data-ttu-id="fa16e-106">O cmdlet **New-AzureStorageTableStoredAccessPolicy** cria uma política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa16e-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="fa16e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa16e-107">EXAMPLES</span></span>

### <span data-ttu-id="fa16e-108">Exemplo 1: criar uma política de acesso armazenada em uma tabela</span><span class="sxs-lookup"><span data-stu-id="fa16e-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="fa16e-109">Esse comando cria uma política de acesso chamada Policy02 na tabela armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="fa16e-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="fa16e-110">OS</span><span class="sxs-lookup"><span data-stu-id="fa16e-110">PARAMETERS</span></span>

### <span data-ttu-id="fa16e-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fa16e-111">-Context</span></span>
<span data-ttu-id="fa16e-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa16e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fa16e-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fa16e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fa16e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa16e-114">-DefaultProfile</span></span>
<span data-ttu-id="fa16e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa16e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa16e-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fa16e-116">-ExpiryTime</span></span>
<span data-ttu-id="fa16e-117">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="fa16e-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="fa16e-118">-Permissão</span><span class="sxs-lookup"><span data-stu-id="fa16e-118">-Permission</span></span>
<span data-ttu-id="fa16e-119">Especifica as permissões na política de acesso armazenado para acessar a tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fa16e-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="fa16e-120">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="fa16e-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="fa16e-121">-Política</span><span class="sxs-lookup"><span data-stu-id="fa16e-121">-Policy</span></span>
<span data-ttu-id="fa16e-122">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="fa16e-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="fa16e-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fa16e-123">-StartTime</span></span>
<span data-ttu-id="fa16e-124">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="fa16e-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="fa16e-125">-Tabela</span><span class="sxs-lookup"><span data-stu-id="fa16e-125">-Table</span></span>
<span data-ttu-id="fa16e-126">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa16e-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="fa16e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa16e-127">CommonParameters</span></span>
<span data-ttu-id="fa16e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa16e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa16e-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa16e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa16e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa16e-130">INPUTS</span></span>

### <span data-ttu-id="fa16e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fa16e-131">System.String</span></span>

### <span data-ttu-id="fa16e-132">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa16e-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fa16e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa16e-133">OUTPUTS</span></span>

### <span data-ttu-id="fa16e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fa16e-134">System.String</span></span>

## <span data-ttu-id="fa16e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa16e-135">NOTES</span></span>

## <span data-ttu-id="fa16e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa16e-136">RELATED LINKS</span></span>

[<span data-ttu-id="fa16e-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa16e-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fa16e-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa16e-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fa16e-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa16e-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fa16e-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa16e-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


