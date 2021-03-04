---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: c85b482ff077263d20ae770e6ec6d91b497153e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890916"
---
# <span data-ttu-id="e9fc0-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e9fc0-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="e9fc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fc0-103">Cria um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e9fc0-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="e9fc0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e9fc0-104">SYNTAX</span></span>

### <span data-ttu-id="e9fc0-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e9fc0-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9fc0-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e9fc0-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9fc0-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e9fc0-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9fc0-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e9fc0-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9fc0-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e9fc0-109">DESCRIPTION</span></span>
<span data-ttu-id="e9fc0-110">O cmdlet **New-AzRmStorageContainer** cria um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e9fc0-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="e9fc0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9fc0-111">EXAMPLES</span></span>

### <span data-ttu-id="e9fc0-112">Exemplo 1: Criar um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner, com metadados</span><span class="sxs-lookup"><span data-stu-id="e9fc0-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="e9fc0-113">Este comando cria um contêiner de blob armazenamento com nome da conta de armazenamento e nome do contêiner, com metadados.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="e9fc0-114">Exemplo 2: Criar um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner, com acesso público como Blob</span><span class="sxs-lookup"><span data-stu-id="e9fc0-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="e9fc0-115">Este comando cria um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner, com acesso público como Blob.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="e9fc0-116">Exemplo 3: Criar um contêiner de armazenamento com a configuração EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e9fc0-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="e9fc0-117">Este comando cria um contêiner de armazenamento com um encryptionScope defalt e bloqueia a substituição do escopo de criptografia do padrão do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="e9fc0-118">Em seguida, mostre as propriedades de contêiner relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-118">Then show the related container properties.</span></span>

## <span data-ttu-id="e9fc0-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e9fc0-119">PARAMETERS</span></span>

### <span data-ttu-id="e9fc0-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e9fc0-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="e9fc0-121">Padrão do contêiner para usar o escopo de criptografia especificado para todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9fc0-122">-DefaultProfile</span></span>
<span data-ttu-id="e9fc0-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-124">-Metadados</span><span class="sxs-lookup"><span data-stu-id="e9fc0-124">-Metadata</span></span>
<span data-ttu-id="e9fc0-125">Metadados de Contêiner</span><span class="sxs-lookup"><span data-stu-id="e9fc0-125">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e9fc0-126">-Name</span></span>
<span data-ttu-id="e9fc0-127">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="e9fc0-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="e9fc0-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="e9fc0-129">Bloquear a substituição do escopo de criptografia do padrão do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="e9fc0-130">-PublicAccess</span></span>
<span data-ttu-id="e9fc0-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="e9fc0-131">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9fc0-132">-ResourceGroupName</span></span>
<span data-ttu-id="e9fc0-133">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9fc0-134">-StorageAccount</span></span>
<span data-ttu-id="e9fc0-135">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e9fc0-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e9fc0-136">-StorageAccountName</span></span>
<span data-ttu-id="e9fc0-137">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9fc0-138">-Confirm</span></span>
<span data-ttu-id="e9fc0-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9fc0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9fc0-140">-WhatIf</span></span>
<span data-ttu-id="e9fc0-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9fc0-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9fc0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9fc0-143">CommonParameters</span></span>
<span data-ttu-id="e9fc0-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9fc0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9fc0-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9fc0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9fc0-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9fc0-146">INPUTS</span></span>

### <span data-ttu-id="e9fc0-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e9fc0-147">System.String</span></span>

### <span data-ttu-id="e9fc0-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9fc0-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e9fc0-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e9fc0-149">OUTPUTS</span></span>

### <span data-ttu-id="e9fc0-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="e9fc0-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e9fc0-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="e9fc0-151">NOTES</span></span>

## <span data-ttu-id="e9fc0-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9fc0-152">RELATED LINKS</span></span>
