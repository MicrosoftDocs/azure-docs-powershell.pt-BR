---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 901061390c68853832bad14965620abad21817e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116107"
---
# <span data-ttu-id="03b7f-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="03b7f-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="03b7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="03b7f-103">Cria um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="03b7f-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="03b7f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03b7f-104">SYNTAX</span></span>

### <span data-ttu-id="03b7f-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="03b7f-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b7f-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="03b7f-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b7f-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="03b7f-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b7f-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="03b7f-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03b7f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="03b7f-109">DESCRIPTION</span></span>
<span data-ttu-id="03b7f-110">O **cmdlet New-AzRmStorageContainer** cria um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="03b7f-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="03b7f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="03b7f-111">EXAMPLES</span></span>

### <span data-ttu-id="03b7f-112">Exemplo 1: Criar um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner, com metadados</span><span class="sxs-lookup"><span data-stu-id="03b7f-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="03b7f-113">Esse comando cria um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner, com metadados.</span><span class="sxs-lookup"><span data-stu-id="03b7f-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="03b7f-114">Exemplo 2: Criar um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner, com acesso público como Blob</span><span class="sxs-lookup"><span data-stu-id="03b7f-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="03b7f-115">Esse comando cria um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner, com acesso público como Blob.</span><span class="sxs-lookup"><span data-stu-id="03b7f-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="03b7f-116">Exemplo 3: Criar um contêiner de armazenamento com a configuração EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="03b7f-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
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

<span data-ttu-id="03b7f-117">Esse comando cria um contêiner de armazenamento com uma criptografia DefaltScope e bloqueia a substituição do escopo de criptografia do padrão do contêiner.</span><span class="sxs-lookup"><span data-stu-id="03b7f-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="03b7f-118">Em seguida, mostre as propriedades de contêiner relacionadas.</span><span class="sxs-lookup"><span data-stu-id="03b7f-118">Then show the related container properties.</span></span>

## <span data-ttu-id="03b7f-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03b7f-119">PARAMETERS</span></span>

### <span data-ttu-id="03b7f-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="03b7f-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="03b7f-121">Padrão do contêiner para usar escopo de criptografia especificado para todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="03b7f-121">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="03b7f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b7f-122">-DefaultProfile</span></span>
<span data-ttu-id="03b7f-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="03b7f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03b7f-124">-Metadados</span><span class="sxs-lookup"><span data-stu-id="03b7f-124">-Metadata</span></span>
<span data-ttu-id="03b7f-125">Metadados de Contêiner</span><span class="sxs-lookup"><span data-stu-id="03b7f-125">Container Metadata</span></span>

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

### <span data-ttu-id="03b7f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="03b7f-126">-Name</span></span>
<span data-ttu-id="03b7f-127">Nome do Contêiner</span><span class="sxs-lookup"><span data-stu-id="03b7f-127">Container Name</span></span>

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

### <span data-ttu-id="03b7f-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="03b7f-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="03b7f-129">Bloquear a substituição do escopo de criptografia do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="03b7f-129">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="03b7f-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="03b7f-130">-PublicAccess</span></span>
<span data-ttu-id="03b7f-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="03b7f-131">Container PublicAccess</span></span>

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

### <span data-ttu-id="03b7f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b7f-132">-ResourceGroupName</span></span>
<span data-ttu-id="03b7f-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03b7f-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="03b7f-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="03b7f-134">-StorageAccount</span></span>
<span data-ttu-id="03b7f-135">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="03b7f-135">Storage account object</span></span>

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

### <span data-ttu-id="03b7f-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="03b7f-136">-StorageAccountName</span></span>
<span data-ttu-id="03b7f-137">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="03b7f-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="03b7f-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="03b7f-138">-Confirm</span></span>
<span data-ttu-id="03b7f-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b7f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b7f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b7f-140">-WhatIf</span></span>
<span data-ttu-id="03b7f-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="03b7f-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03b7f-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03b7f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b7f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b7f-143">CommonParameters</span></span>
<span data-ttu-id="03b7f-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b7f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b7f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b7f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b7f-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="03b7f-146">INPUTS</span></span>

### <span data-ttu-id="03b7f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="03b7f-147">System.String</span></span>

### <span data-ttu-id="03b7f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="03b7f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="03b7f-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="03b7f-149">OUTPUTS</span></span>

### <span data-ttu-id="03b7f-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="03b7f-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="03b7f-151">Notas</span><span class="sxs-lookup"><span data-stu-id="03b7f-151">NOTES</span></span>

## <span data-ttu-id="03b7f-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03b7f-152">RELATED LINKS</span></span>
