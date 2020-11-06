---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 41ae0d3c985bbb5e1d58f92287fa4a0050dfa738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598525"
---
# <span data-ttu-id="ee49e-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee49e-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="ee49e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee49e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee49e-103">Define a política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee49e-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="ee49e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee49e-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee49e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee49e-105">DESCRIPTION</span></span>
<span data-ttu-id="ee49e-106">O cmdlet **set-AzStorageTableStoredAccessPolicy** define a política de acesso armazenada para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee49e-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="ee49e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee49e-107">EXAMPLES</span></span>

### <span data-ttu-id="ee49e-108">Exemplo 1: definir uma política de acesso armazenado em tabela com permissão completa</span><span class="sxs-lookup"><span data-stu-id="ee49e-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="ee49e-109">Esse comando define uma política de acesso chamada Policy08 para a tabela de armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="ee49e-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="ee49e-110">OS</span><span class="sxs-lookup"><span data-stu-id="ee49e-110">PARAMETERS</span></span>

### <span data-ttu-id="ee49e-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ee49e-111">-Context</span></span>
<span data-ttu-id="ee49e-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee49e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ee49e-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ee49e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ee49e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee49e-114">-DefaultProfile</span></span>
<span data-ttu-id="ee49e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee49e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee49e-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ee49e-116">-ExpiryTime</span></span>
<span data-ttu-id="ee49e-117">Especifica a hora em que a política de acesso armazenado expira.</span><span class="sxs-lookup"><span data-stu-id="ee49e-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="ee49e-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ee49e-118">-NoExpiryTime</span></span>
<span data-ttu-id="ee49e-119">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="ee49e-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee49e-120">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="ee49e-120">-NoStartTime</span></span>
<span data-ttu-id="ee49e-121">Indica que a hora de início está definida como $Null.</span><span class="sxs-lookup"><span data-stu-id="ee49e-121">Indicates that the start time is set to $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee49e-122">-Permissão</span><span class="sxs-lookup"><span data-stu-id="ee49e-122">-Permission</span></span>
<span data-ttu-id="ee49e-123">Especifica as permissões na política de acesso armazenado para acessar a tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ee49e-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="ee49e-124">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="ee49e-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ee49e-125">-Política</span><span class="sxs-lookup"><span data-stu-id="ee49e-125">-Policy</span></span>
<span data-ttu-id="ee49e-126">Especifica o nome da política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="ee49e-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="ee49e-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ee49e-127">-StartTime</span></span>
<span data-ttu-id="ee49e-128">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="ee49e-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ee49e-129">-Tabela</span><span class="sxs-lookup"><span data-stu-id="ee49e-129">-Table</span></span>
<span data-ttu-id="ee49e-130">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee49e-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="ee49e-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee49e-131">-Confirm</span></span>
<span data-ttu-id="ee49e-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee49e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee49e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee49e-133">-WhatIf</span></span>
<span data-ttu-id="ee49e-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee49e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee49e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee49e-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee49e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee49e-136">CommonParameters</span></span>
<span data-ttu-id="ee49e-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee49e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee49e-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee49e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee49e-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee49e-139">INPUTS</span></span>

### <span data-ttu-id="ee49e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ee49e-140">System.String</span></span>

### <span data-ttu-id="ee49e-141">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee49e-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ee49e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee49e-142">OUTPUTS</span></span>

### <span data-ttu-id="ee49e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ee49e-143">System.String</span></span>

## <span data-ttu-id="ee49e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee49e-144">NOTES</span></span>

## <span data-ttu-id="ee49e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee49e-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee49e-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee49e-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ee49e-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee49e-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ee49e-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee49e-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ee49e-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee49e-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
