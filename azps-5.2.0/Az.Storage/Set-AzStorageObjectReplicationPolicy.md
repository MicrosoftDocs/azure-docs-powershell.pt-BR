---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260754"
---
# <span data-ttu-id="f779b-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f779b-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="f779b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f779b-102">SYNOPSIS</span></span>
<span data-ttu-id="f779b-103">Cria ou atualiza a política de replicação de objetos especificada em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f779b-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="f779b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f779b-104">SYNTAX</span></span>

### <span data-ttu-id="f779b-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f779b-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f779b-106">Políticaobject</span><span class="sxs-lookup"><span data-stu-id="f779b-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f779b-107">Accountobject</span><span class="sxs-lookup"><span data-stu-id="f779b-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f779b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f779b-108">DESCRIPTION</span></span>
<span data-ttu-id="f779b-109">O cmdlet **set-AzStorageObjectReplicationPolicy** cria ou atualiza a política de replicação de objetos especificada em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f779b-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="f779b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f779b-110">EXAMPLES</span></span>

### <span data-ttu-id="f779b-111">Exemplo 1: definir a política de replicação de objetos para a conta de destino e de origem.</span><span class="sxs-lookup"><span data-stu-id="f779b-111">Example 1: Set object replication policy to both destination and source account.</span></span>
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

<span data-ttu-id="f779b-112">Este comando define a política de replicação de objetos para a conta de destino e de origem.</span><span class="sxs-lookup"><span data-stu-id="f779b-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="f779b-113">Primeiro, crie duas regras de política de replicação de objetos e defina a política com as 2 regras para a conta de destino.</span><span class="sxs-lookup"><span data-stu-id="f779b-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="f779b-114">Em seguida, defina a política de replicação de objeto da conta de destino para a conta de origem.</span><span class="sxs-lookup"><span data-stu-id="f779b-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="f779b-115">OS</span><span class="sxs-lookup"><span data-stu-id="f779b-115">PARAMETERS</span></span>

### <span data-ttu-id="f779b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f779b-116">-DefaultProfile</span></span>
<span data-ttu-id="f779b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f779b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f779b-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="f779b-118">-DestinationAccount</span></span>
<span data-ttu-id="f779b-119">Política de replicação de objeto DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="f779b-119">Object Replication Policy DestinationAccount.</span></span>

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

### <span data-ttu-id="f779b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f779b-120">-InputObject</span></span>
<span data-ttu-id="f779b-121">Objeto de política de replicação de objeto a ser definido para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="f779b-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="f779b-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="f779b-122">-PolicyId</span></span>
<span data-ttu-id="f779b-123">ID da política de replicação de objetos. Ele deve ser um GUID ou ' default '.</span><span class="sxs-lookup"><span data-stu-id="f779b-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="f779b-124">Se não inserir PolicyId, usará ' default ', o que significa criar uma nova política e a ID da nova política será retornada na política criada.</span><span class="sxs-lookup"><span data-stu-id="f779b-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

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

### <span data-ttu-id="f779b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f779b-125">-ResourceGroupName</span></span>
<span data-ttu-id="f779b-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f779b-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="f779b-127">-Regra</span><span class="sxs-lookup"><span data-stu-id="f779b-127">-Rule</span></span>
<span data-ttu-id="f779b-128">Regras de política de replicação de objetos.</span><span class="sxs-lookup"><span data-stu-id="f779b-128">Object Replication Policy Rules.</span></span>

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

### <span data-ttu-id="f779b-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="f779b-129">-SourceAccount</span></span>
<span data-ttu-id="f779b-130">Política de replicação de objeto SourceAccount.</span><span class="sxs-lookup"><span data-stu-id="f779b-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="f779b-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f779b-131">-StorageAccount</span></span>
<span data-ttu-id="f779b-132">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f779b-132">Storage account object</span></span>

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

### <span data-ttu-id="f779b-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f779b-133">-StorageAccountName</span></span>
<span data-ttu-id="f779b-134">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f779b-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="f779b-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f779b-135">-Confirm</span></span>
<span data-ttu-id="f779b-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f779b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f779b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f779b-137">-WhatIf</span></span>
<span data-ttu-id="f779b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f779b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f779b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f779b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f779b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f779b-140">CommonParameters</span></span>
<span data-ttu-id="f779b-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f779b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f779b-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f779b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f779b-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f779b-143">INPUTS</span></span>

### <span data-ttu-id="f779b-144">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f779b-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f779b-145">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f779b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="f779b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f779b-146">OUTPUTS</span></span>

### <span data-ttu-id="f779b-147">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f779b-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="f779b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f779b-148">NOTES</span></span>

## <span data-ttu-id="f779b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f779b-149">RELATED LINKS</span></span>
