---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 609dd0d8732ac83836596ecee9f95cd8d7df3f27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610954"
---
# <span data-ttu-id="68c8a-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68c8a-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="68c8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="68c8a-103">Define a política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68c8a-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68c8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68c8a-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68c8a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="68c8a-106">O cmdlet **set-AzureStorageTableStoredAccessPolicy** define a política de acesso armazenada para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68c8a-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="68c8a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68c8a-107">EXAMPLES</span></span>

### <span data-ttu-id="68c8a-108">Exemplo 1: definir uma política de acesso armazenado em tabela com permissão completa</span><span class="sxs-lookup"><span data-stu-id="68c8a-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="68c8a-109">Esse comando define uma política de acesso chamada Policy08 para a tabela de armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="68c8a-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="68c8a-110">OS</span><span class="sxs-lookup"><span data-stu-id="68c8a-110">PARAMETERS</span></span>

### <span data-ttu-id="68c8a-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="68c8a-111">-Context</span></span>
<span data-ttu-id="68c8a-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68c8a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="68c8a-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="68c8a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="68c8a-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="68c8a-114">-ExpiryTime</span></span>
<span data-ttu-id="68c8a-115">Especifica a hora em que a política de acesso armazenado expira.</span><span class="sxs-lookup"><span data-stu-id="68c8a-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="68c8a-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="68c8a-116">-NoExpiryTime</span></span>
<span data-ttu-id="68c8a-117">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="68c8a-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c8a-118">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="68c8a-118">-NoStartTime</span></span>
<span data-ttu-id="68c8a-119">Indica que a hora de início está definida como $Null.</span><span class="sxs-lookup"><span data-stu-id="68c8a-119">Indicates that the start time is set to $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c8a-120">-Permissão</span><span class="sxs-lookup"><span data-stu-id="68c8a-120">-Permission</span></span>
<span data-ttu-id="68c8a-121">Especifica as permissões na política de acesso armazenado para acessar a tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="68c8a-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="68c8a-122">-Política</span><span class="sxs-lookup"><span data-stu-id="68c8a-122">-Policy</span></span>
<span data-ttu-id="68c8a-123">Especifica o nome da política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="68c8a-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="68c8a-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="68c8a-124">-StartTime</span></span>
<span data-ttu-id="68c8a-125">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="68c8a-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="68c8a-126">-Tabela</span><span class="sxs-lookup"><span data-stu-id="68c8a-126">-Table</span></span>
<span data-ttu-id="68c8a-127">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68c8a-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="68c8a-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68c8a-128">-Confirm</span></span>
<span data-ttu-id="68c8a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68c8a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c8a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68c8a-130">-WhatIf</span></span>
<span data-ttu-id="68c8a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68c8a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68c8a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68c8a-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c8a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c8a-133">CommonParameters</span></span>
<span data-ttu-id="68c8a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68c8a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c8a-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68c8a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c8a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68c8a-136">INPUTS</span></span>

### <span data-ttu-id="68c8a-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="68c8a-137">IStorageContext</span></span>

<span data-ttu-id="68c8a-138">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="68c8a-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="68c8a-139">String</span><span class="sxs-lookup"><span data-stu-id="68c8a-139">String</span></span>

<span data-ttu-id="68c8a-140">O parâmetro ' Table ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="68c8a-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="68c8a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68c8a-141">OUTPUTS</span></span>

### <span data-ttu-id="68c8a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="68c8a-142">System.String</span></span>

## <span data-ttu-id="68c8a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68c8a-143">NOTES</span></span>

## <span data-ttu-id="68c8a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68c8a-144">RELATED LINKS</span></span>

[<span data-ttu-id="68c8a-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68c8a-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="68c8a-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="68c8a-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="68c8a-147">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68c8a-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="68c8a-148">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68c8a-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
