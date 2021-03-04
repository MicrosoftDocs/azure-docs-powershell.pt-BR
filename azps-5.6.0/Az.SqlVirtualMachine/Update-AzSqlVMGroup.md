---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 04a75ec50f985bb1cea0266c077946adbdab4f65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891555"
---
# <span data-ttu-id="79a40-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="79a40-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="79a40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a40-102">SYNOPSIS</span></span>
<span data-ttu-id="79a40-103">Atualiza um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="79a40-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="79a40-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="79a40-104">SYNTAX</span></span>

### <span data-ttu-id="79a40-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="79a40-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a40-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="79a40-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a40-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="79a40-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a40-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="79a40-108">DESCRIPTION</span></span>
<span data-ttu-id="79a40-109">O Update-AzSqlVMGroup atualiza um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="79a40-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="79a40-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79a40-110">EXAMPLES</span></span>

### <span data-ttu-id="79a40-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79a40-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="79a40-112">Atualiza as marcas de um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="79a40-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="79a40-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="79a40-113">PARAMETERS</span></span>

### <span data-ttu-id="79a40-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79a40-114">-AsJob</span></span>
<span data-ttu-id="79a40-115">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="79a40-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="79a40-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="79a40-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="79a40-117">Nome usado para criar cluster</span><span class="sxs-lookup"><span data-stu-id="79a40-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="79a40-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="79a40-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="79a40-119">Nome usado para cluster operacional</span><span class="sxs-lookup"><span data-stu-id="79a40-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="79a40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a40-120">-DefaultProfile</span></span>
<span data-ttu-id="79a40-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79a40-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a40-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="79a40-122">-DomainFqdn</span></span>
<span data-ttu-id="79a40-123">Nome totalmente qualificado do domínio</span><span class="sxs-lookup"><span data-stu-id="79a40-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="79a40-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="79a40-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="79a40-125">Caminho opcional para testemunha de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="79a40-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="79a40-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79a40-126">-InputObject</span></span>
<span data-ttu-id="79a40-127">SQL objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79a40-127">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79a40-128">-Name</span><span class="sxs-lookup"><span data-stu-id="79a40-128">-Name</span></span>
<span data-ttu-id="79a40-129">SQL nome do grupo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79a40-129">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a40-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="79a40-130">-OuPath</span></span>
<span data-ttu-id="79a40-131">Caminho da Unidade Organizacional no qual os nós e o cluster estarão presentes</span><span class="sxs-lookup"><span data-stu-id="79a40-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="79a40-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a40-132">-ResourceGroupName</span></span>
<span data-ttu-id="79a40-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="79a40-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a40-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79a40-134">-ResourceId</span></span>
<span data-ttu-id="79a40-135">SQL id de recurso do grupo de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="79a40-135">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a40-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="79a40-136">-SqlServiceAccount</span></span>
<span data-ttu-id="79a40-137">Nome em que SQL serviço será executado em todas as SQL virtuais participantes no cluster</span><span class="sxs-lookup"><span data-stu-id="79a40-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="79a40-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="79a40-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="79a40-139">Chave primária da conta de armazenamento testemunha</span><span class="sxs-lookup"><span data-stu-id="79a40-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a40-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="79a40-140">-StorageAccountUrl</span></span>
<span data-ttu-id="79a40-141">Chave primária da conta de armazenamento testemunha</span><span class="sxs-lookup"><span data-stu-id="79a40-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="79a40-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="79a40-142">-Tag</span></span>
<span data-ttu-id="79a40-143">As marcas a associar ao grupo SQL máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79a40-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="79a40-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79a40-144">-Confirm</span></span>
<span data-ttu-id="79a40-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a40-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a40-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a40-146">-WhatIf</span></span>
<span data-ttu-id="79a40-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79a40-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a40-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79a40-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a40-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a40-149">CommonParameters</span></span>
<span data-ttu-id="79a40-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a40-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a40-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79a40-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a40-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79a40-152">INPUTS</span></span>

### <span data-ttu-id="79a40-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="79a40-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="79a40-154">System.String</span><span class="sxs-lookup"><span data-stu-id="79a40-154">System.String</span></span>

## <span data-ttu-id="79a40-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="79a40-155">OUTPUTS</span></span>

### <span data-ttu-id="79a40-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="79a40-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="79a40-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="79a40-157">NOTES</span></span>

## <span data-ttu-id="79a40-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79a40-158">RELATED LINKS</span></span>
