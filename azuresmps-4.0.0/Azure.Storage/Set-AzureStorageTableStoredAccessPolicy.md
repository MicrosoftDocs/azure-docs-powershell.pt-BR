---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426202"
---
# <span data-ttu-id="e0bf9-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0bf9-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="e0bf9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bf9-103">Define a política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="e0bf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0bf9-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0bf9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="e0bf9-106">O cmdlet **set-AzureStorageTableStoredAccessPolicy** define a política de acesso armazenada para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="e0bf9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0bf9-107">EXAMPLES</span></span>

### <span data-ttu-id="e0bf9-108">Exemplo 1: definir uma política de acesso armazenado em tabela com permissão completa</span><span class="sxs-lookup"><span data-stu-id="e0bf9-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="e0bf9-109">Esse comando define uma política de acesso chamada Policy08 para a tabela de armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="e0bf9-110">OS</span><span class="sxs-lookup"><span data-stu-id="e0bf9-110">PARAMETERS</span></span>

### <span data-ttu-id="e0bf9-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e0bf9-111">-Context</span></span>
<span data-ttu-id="e0bf9-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e0bf9-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e0bf9-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e0bf9-114">-ExpiryTime</span></span>
<span data-ttu-id="e0bf9-115">Especifica a hora em que a política de acesso armazenado expira.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="e0bf9-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e0bf9-116">-NoExpiryTime</span></span>
<span data-ttu-id="e0bf9-117">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="e0bf9-118">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="e0bf9-118">-NoStartTime</span></span>
<span data-ttu-id="e0bf9-119">Indica que a hora de início está definida como $Null.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="e0bf9-120">-Permissão</span><span class="sxs-lookup"><span data-stu-id="e0bf9-120">-Permission</span></span>
<span data-ttu-id="e0bf9-121">Especifica o nível de acesso público a essa tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-121">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="e0bf9-122">-Política</span><span class="sxs-lookup"><span data-stu-id="e0bf9-122">-Policy</span></span>
<span data-ttu-id="e0bf9-123">Especifica uma política de acesso armazenado, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="e0bf9-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e0bf9-124">-StartTime</span></span>
<span data-ttu-id="e0bf9-125">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="e0bf9-126">-Tabela</span><span class="sxs-lookup"><span data-stu-id="e0bf9-126">-Table</span></span>
<span data-ttu-id="e0bf9-127">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="e0bf9-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0bf9-128">-Confirm</span></span>
<span data-ttu-id="e0bf9-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0bf9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0bf9-130">-WhatIf</span></span>
<span data-ttu-id="e0bf9-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0bf9-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0bf9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bf9-133">CommonParameters</span></span>
<span data-ttu-id="e0bf9-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0bf9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bf9-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0bf9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bf9-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0bf9-136">INPUTS</span></span>

## <span data-ttu-id="e0bf9-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0bf9-137">OUTPUTS</span></span>

## <span data-ttu-id="e0bf9-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0bf9-138">NOTES</span></span>

## <span data-ttu-id="e0bf9-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0bf9-139">RELATED LINKS</span></span>

[<span data-ttu-id="e0bf9-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0bf9-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="e0bf9-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e0bf9-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e0bf9-142">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0bf9-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="e0bf9-143">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0bf9-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
