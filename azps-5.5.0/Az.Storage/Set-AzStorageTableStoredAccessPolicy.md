---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 822781f6c46eeb76a953eaa66935c03cd76df737
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118563"
---
# <span data-ttu-id="68dd5-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68dd5-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="68dd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="68dd5-103">Define a política de acesso armazenada para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68dd5-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="68dd5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68dd5-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68dd5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="68dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="68dd5-106">O cmdlet **Set-AzStorageTableStoredAccessPolicy** definiu a política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68dd5-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="68dd5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="68dd5-107">EXAMPLES</span></span>

### <span data-ttu-id="68dd5-108">Exemplo 1: Definir uma política de acesso armazenada na tabela com permissão total</span><span class="sxs-lookup"><span data-stu-id="68dd5-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="68dd5-109">Esse comando define uma política de acesso chamada Política08 para tabela de armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="68dd5-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="68dd5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68dd5-110">PARAMETERS</span></span>

### <span data-ttu-id="68dd5-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="68dd5-111">-Context</span></span>
<span data-ttu-id="68dd5-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68dd5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="68dd5-113">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68dd5-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="68dd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68dd5-114">-DefaultProfile</span></span>
<span data-ttu-id="68dd5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68dd5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68dd5-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="68dd5-116">-ExpiryTime</span></span>
<span data-ttu-id="68dd5-117">Especifica o tempo em que a política de acesso armazenada expira.</span><span class="sxs-lookup"><span data-stu-id="68dd5-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="68dd5-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="68dd5-118">-NoExpiryTime</span></span>
<span data-ttu-id="68dd5-119">Indica que a política de acesso não tem data de validade.</span><span class="sxs-lookup"><span data-stu-id="68dd5-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="68dd5-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="68dd5-120">-NoStartTime</span></span>
<span data-ttu-id="68dd5-121">Indica que a hora de início está definida como $Null.</span><span class="sxs-lookup"><span data-stu-id="68dd5-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="68dd5-122">-Permissão</span><span class="sxs-lookup"><span data-stu-id="68dd5-122">-Permission</span></span>
<span data-ttu-id="68dd5-123">Especifica permissões na política de acesso armazenada para acessar a tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="68dd5-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="68dd5-124">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).</span><span class="sxs-lookup"><span data-stu-id="68dd5-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="68dd5-125">-Política</span><span class="sxs-lookup"><span data-stu-id="68dd5-125">-Policy</span></span>
<span data-ttu-id="68dd5-126">Especifica o nome da política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="68dd5-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="68dd5-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="68dd5-127">-StartTime</span></span>
<span data-ttu-id="68dd5-128">Especifica o momento em que a política de acesso armazenada se torna válida.</span><span class="sxs-lookup"><span data-stu-id="68dd5-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="68dd5-129">-Tabela</span><span class="sxs-lookup"><span data-stu-id="68dd5-129">-Table</span></span>
<span data-ttu-id="68dd5-130">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="68dd5-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="68dd5-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="68dd5-131">-Confirm</span></span>
<span data-ttu-id="68dd5-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68dd5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68dd5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68dd5-133">-WhatIf</span></span>
<span data-ttu-id="68dd5-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="68dd5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68dd5-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68dd5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68dd5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68dd5-136">CommonParameters</span></span>
<span data-ttu-id="68dd5-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68dd5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68dd5-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68dd5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68dd5-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="68dd5-139">INPUTS</span></span>

### <span data-ttu-id="68dd5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="68dd5-140">System.String</span></span>

### <span data-ttu-id="68dd5-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="68dd5-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="68dd5-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="68dd5-142">OUTPUTS</span></span>

### <span data-ttu-id="68dd5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="68dd5-143">System.String</span></span>

## <span data-ttu-id="68dd5-144">Notas</span><span class="sxs-lookup"><span data-stu-id="68dd5-144">NOTES</span></span>

## <span data-ttu-id="68dd5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68dd5-145">RELATED LINKS</span></span>

[<span data-ttu-id="68dd5-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68dd5-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="68dd5-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="68dd5-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="68dd5-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68dd5-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="68dd5-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68dd5-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
