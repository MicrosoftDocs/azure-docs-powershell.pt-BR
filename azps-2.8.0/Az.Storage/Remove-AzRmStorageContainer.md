---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774213"
---
# <span data-ttu-id="4a485-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4a485-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="4a485-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a485-102">SYNOPSIS</span></span>
<span data-ttu-id="4a485-103">Remove um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4a485-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="4a485-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a485-104">SYNTAX</span></span>

### <span data-ttu-id="4a485-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a485-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a485-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="4a485-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a485-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="4a485-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a485-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a485-108">DESCRIPTION</span></span>
<span data-ttu-id="4a485-109">O cmdlet **Remove-AzRmStorageContainer** remove um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4a485-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="4a485-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a485-110">EXAMPLES</span></span>

### <span data-ttu-id="4a485-111">Exemplo 1: remover um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="4a485-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="4a485-112">Esse comando Remove um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4a485-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="4a485-113">Exemplo 2: remover um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="4a485-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="4a485-114">Esse comando Remove um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4a485-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="4a485-115">Exemplo 3: remover todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="4a485-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="4a485-116">Esse comando Remove todos os contêineres de armazenamento de BLOB em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a485-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="4a485-117">OS</span><span class="sxs-lookup"><span data-stu-id="4a485-117">PARAMETERS</span></span>

### <span data-ttu-id="4a485-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a485-118">-DefaultProfile</span></span>
<span data-ttu-id="4a485-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a485-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a485-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4a485-120">-Force</span></span>
<span data-ttu-id="4a485-121">Forçar a remoção do contêiner e todo o conteúdo dele</span><span class="sxs-lookup"><span data-stu-id="4a485-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a485-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a485-122">-InputObject</span></span>
<span data-ttu-id="4a485-123">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4a485-123">Storage container object</span></span>

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

### <span data-ttu-id="4a485-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a485-124">-Name</span></span>
<span data-ttu-id="4a485-125">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="4a485-125">Container Name</span></span>

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

### <span data-ttu-id="4a485-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a485-126">-PassThru</span></span>
<span data-ttu-id="4a485-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="4a485-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4a485-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a485-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a485-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a485-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a485-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a485-130">-StorageAccount</span></span>
<span data-ttu-id="4a485-131">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4a485-131">Storage account object</span></span>

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

### <span data-ttu-id="4a485-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4a485-132">-StorageAccountName</span></span>
<span data-ttu-id="4a485-133">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4a485-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="4a485-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a485-134">-Confirm</span></span>
<span data-ttu-id="4a485-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a485-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a485-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a485-136">-WhatIf</span></span>
<span data-ttu-id="4a485-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a485-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a485-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a485-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a485-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a485-139">CommonParameters</span></span>
<span data-ttu-id="4a485-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a485-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a485-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a485-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a485-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a485-142">INPUTS</span></span>

### <span data-ttu-id="4a485-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4a485-143">System.String</span></span>

### <span data-ttu-id="4a485-144">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4a485-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4a485-145">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="4a485-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="4a485-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a485-146">OUTPUTS</span></span>

### <span data-ttu-id="4a485-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a485-147">System.Boolean</span></span>

## <span data-ttu-id="4a485-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a485-148">NOTES</span></span>

## <span data-ttu-id="4a485-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a485-149">RELATED LINKS</span></span>