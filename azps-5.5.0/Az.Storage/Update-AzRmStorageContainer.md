---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114387"
---
# <span data-ttu-id="7efc1-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7efc1-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="7efc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7efc1-102">SYNOPSIS</span></span>
<span data-ttu-id="7efc1-103">Modifica um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="7efc1-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="7efc1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7efc1-104">SYNTAX</span></span>

### <span data-ttu-id="7efc1-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7efc1-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7efc1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7efc1-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7efc1-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="7efc1-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7efc1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7efc1-108">DESCRIPTION</span></span>
<span data-ttu-id="7efc1-109">O cmdlet **Update-AzRmStorageContainer** modifica um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="7efc1-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="7efc1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7efc1-110">EXAMPLES</span></span>

### <span data-ttu-id="7efc1-111">Exemplo 1: modifica os metadados de um contêiner de blob de armazenamento e o acesso público com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="7efc1-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="7efc1-112">Esse comando modifica os metadados de um contêiner de blob armazenamento e o acesso público com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7efc1-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="7efc1-113">Exemplo 2: Desabilitar o acesso público em um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="7efc1-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="7efc1-114">Esse comando desabilita o acesso público em um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7efc1-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="7efc1-115">Exemplo 3: Definir o acesso público como Blob para todos os contêineres de blob armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="7efc1-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="7efc1-116">Esse comando definirá o acesso público como Blob para todos os contêineres de blob de Armazenamento em uma conta de Armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="7efc1-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="7efc1-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7efc1-117">PARAMETERS</span></span>

### <span data-ttu-id="7efc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efc1-118">-DefaultProfile</span></span>
<span data-ttu-id="7efc1-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7efc1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7efc1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7efc1-120">-InputObject</span></span>
<span data-ttu-id="7efc1-121">Objeto de contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7efc1-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7efc1-122">-Metadados</span><span class="sxs-lookup"><span data-stu-id="7efc1-122">-Metadata</span></span>
<span data-ttu-id="7efc1-123">Metadados de Contêiner</span><span class="sxs-lookup"><span data-stu-id="7efc1-123">Container Metadata</span></span>

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

### <span data-ttu-id="7efc1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7efc1-124">-Name</span></span>
<span data-ttu-id="7efc1-125">Nome do Contêiner</span><span class="sxs-lookup"><span data-stu-id="7efc1-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7efc1-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="7efc1-126">-PublicAccess</span></span>
<span data-ttu-id="7efc1-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="7efc1-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="7efc1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7efc1-128">-ResourceGroupName</span></span>
<span data-ttu-id="7efc1-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7efc1-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7efc1-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7efc1-130">-StorageAccount</span></span>
<span data-ttu-id="7efc1-131">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7efc1-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7efc1-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7efc1-132">-StorageAccountName</span></span>
<span data-ttu-id="7efc1-133">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7efc1-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7efc1-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7efc1-134">-Confirm</span></span>
<span data-ttu-id="7efc1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efc1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7efc1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7efc1-136">-WhatIf</span></span>
<span data-ttu-id="7efc1-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7efc1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7efc1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7efc1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7efc1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efc1-139">CommonParameters</span></span>
<span data-ttu-id="7efc1-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7efc1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efc1-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efc1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efc1-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="7efc1-142">INPUTS</span></span>

### <span data-ttu-id="7efc1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7efc1-143">System.String</span></span>

### <span data-ttu-id="7efc1-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7efc1-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7efc1-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="7efc1-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="7efc1-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="7efc1-146">OUTPUTS</span></span>

### <span data-ttu-id="7efc1-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="7efc1-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="7efc1-148">Notas</span><span class="sxs-lookup"><span data-stu-id="7efc1-148">NOTES</span></span>

## <span data-ttu-id="7efc1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7efc1-149">RELATED LINKS</span></span>
