---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: e5d141672fe2f620fc86306b79069d309235393f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888155"
---
# <span data-ttu-id="e5be8-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="e5be8-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="e5be8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5be8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5be8-103">Cria ou atualiza a política de replicação de objeto especificada em uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5be8-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="e5be8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e5be8-104">SYNTAX</span></span>

### <span data-ttu-id="e5be8-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e5be8-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5be8-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="e5be8-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5be8-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e5be8-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5be8-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5be8-108">DESCRIPTION</span></span>
<span data-ttu-id="e5be8-109">O cmdlet **Set-AzStorageObjectReplicationPolicy** cria ou atualiza a política de replicação de objeto especificada em uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5be8-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="e5be8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5be8-110">EXAMPLES</span></span>

### <span data-ttu-id="e5be8-111">Exemplo 1: definir a política de replicação de objeto para a conta de destino e de origem.</span><span class="sxs-lookup"><span data-stu-id="e5be8-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="e5be8-112">Este comando define a política de replicação de objeto como conta de destino e de origem.</span><span class="sxs-lookup"><span data-stu-id="e5be8-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="e5be8-113">Primeiro crie duas regras de política de replicação de objeto e de definir a política com as 2 regras como conta de destino.</span><span class="sxs-lookup"><span data-stu-id="e5be8-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="e5be8-114">Em seguida, de definir a política de replicação de objeto da conta de destino para a conta de origem.</span><span class="sxs-lookup"><span data-stu-id="e5be8-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="e5be8-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e5be8-115">PARAMETERS</span></span>

### <span data-ttu-id="e5be8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5be8-116">-DefaultProfile</span></span>
<span data-ttu-id="e5be8-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5be8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5be8-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="e5be8-118">-DestinationAccount</span></span>
<span data-ttu-id="e5be8-119">Destino da Política de Replicação de ObjetoConta.</span><span class="sxs-lookup"><span data-stu-id="e5be8-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5be8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5be8-120">-InputObject</span></span>
<span data-ttu-id="e5be8-121">Objeto de Política de Replicação de Objeto a ser definido como a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="e5be8-121">Object Replication Policy Object to Set to the specified Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5be8-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="e5be8-122">-PolicyId</span></span>
<span data-ttu-id="e5be8-123">ID da Política de Replicação de Objeto. Deve ser um GUID ou um "padrão".</span><span class="sxs-lookup"><span data-stu-id="e5be8-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="e5be8-124">Se não inserir o PolicyId, usará "padrão", o que significa criar uma nova política e a ID da nova política será retornada na política criada.</span><span class="sxs-lookup"><span data-stu-id="e5be8-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5be8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5be8-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5be8-126">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e5be8-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5be8-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="e5be8-127">-Rule</span></span>
<span data-ttu-id="e5be8-128">Regras de Política de Replicação de Objeto.</span><span class="sxs-lookup"><span data-stu-id="e5be8-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5be8-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="e5be8-129">-SourceAccount</span></span>
<span data-ttu-id="e5be8-130">Object Replication Policy SourceAccount.</span><span class="sxs-lookup"><span data-stu-id="e5be8-130">Object Replication Policy SourceAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5be8-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5be8-131">-StorageAccount</span></span>
<span data-ttu-id="e5be8-132">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e5be8-132">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5be8-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e5be8-133">-StorageAccountName</span></span>
<span data-ttu-id="e5be8-134">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5be8-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5be8-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5be8-135">-Confirm</span></span>
<span data-ttu-id="e5be8-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5be8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5be8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5be8-137">-WhatIf</span></span>
<span data-ttu-id="e5be8-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5be8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5be8-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5be8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5be8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5be8-140">CommonParameters</span></span>
<span data-ttu-id="e5be8-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5be8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5be8-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5be8-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5be8-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5be8-143">INPUTS</span></span>

### <span data-ttu-id="e5be8-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5be8-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e5be8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="e5be8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="e5be8-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e5be8-146">OUTPUTS</span></span>

### <span data-ttu-id="e5be8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="e5be8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="e5be8-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="e5be8-148">NOTES</span></span>

## <span data-ttu-id="e5be8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5be8-149">RELATED LINKS</span></span>
