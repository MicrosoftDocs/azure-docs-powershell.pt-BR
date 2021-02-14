---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115687"
---
# <span data-ttu-id="619e6-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="619e6-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="619e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="619e6-102">SYNOPSIS</span></span>
<span data-ttu-id="619e6-103">Atualiza um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="619e6-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="619e6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="619e6-104">SYNTAX</span></span>

### <span data-ttu-id="619e6-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="619e6-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="619e6-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="619e6-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="619e6-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="619e6-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="619e6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="619e6-108">DESCRIPTION</span></span>
<span data-ttu-id="619e6-109">O Update-AzSqlVMGroup cmdlet atualiza um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="619e6-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="619e6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="619e6-110">EXAMPLES</span></span>

### <span data-ttu-id="619e6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="619e6-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="619e6-112">Atualiza as marcas de um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="619e6-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="619e6-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="619e6-113">PARAMETERS</span></span>

### <span data-ttu-id="619e6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="619e6-114">-AsJob</span></span>
<span data-ttu-id="619e6-115">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="619e6-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="619e6-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="619e6-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="619e6-117">Nome usado para criar cluster</span><span class="sxs-lookup"><span data-stu-id="619e6-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="619e6-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="619e6-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="619e6-119">Nome usado para o cluster operacional</span><span class="sxs-lookup"><span data-stu-id="619e6-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="619e6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619e6-120">-DefaultProfile</span></span>
<span data-ttu-id="619e6-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="619e6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="619e6-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="619e6-122">-DomainFqdn</span></span>
<span data-ttu-id="619e6-123">Nome totalmente qualificado do domínio</span><span class="sxs-lookup"><span data-stu-id="619e6-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="619e6-124">-FileSharePath</span><span class="sxs-lookup"><span data-stu-id="619e6-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="619e6-125">Caminho opcional para a prova de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="619e6-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="619e6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="619e6-126">-InputObject</span></span>
<span data-ttu-id="619e6-127">Objeto de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="619e6-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="619e6-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="619e6-128">-Name</span></span>
<span data-ttu-id="619e6-129">Nome do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="619e6-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="619e6-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="619e6-130">-OuPath</span></span>
<span data-ttu-id="619e6-131">Caminho da Unidade Organizacional no qual os nós e o cluster estarão presentes</span><span class="sxs-lookup"><span data-stu-id="619e6-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="619e6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="619e6-132">-ResourceGroupName</span></span>
<span data-ttu-id="619e6-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="619e6-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="619e6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="619e6-134">-ResourceId</span></span>
<span data-ttu-id="619e6-135">ID do recurso do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="619e6-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="619e6-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="619e6-136">-SqlServiceAccount</span></span>
<span data-ttu-id="619e6-137">Nome sob o qual o serviço SQL será executado em todas as máquinas virtuais SQL participantes no cluster</span><span class="sxs-lookup"><span data-stu-id="619e6-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="619e6-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="619e6-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="619e6-139">Chave primária da conta de armazenamento de informações</span><span class="sxs-lookup"><span data-stu-id="619e6-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="619e6-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="619e6-140">-StorageAccountUrl</span></span>
<span data-ttu-id="619e6-141">Chave primária da conta de armazenamento de informações</span><span class="sxs-lookup"><span data-stu-id="619e6-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="619e6-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="619e6-142">-Tag</span></span>
<span data-ttu-id="619e6-143">As marcas a associar ao grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="619e6-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="619e6-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="619e6-144">-Confirm</span></span>
<span data-ttu-id="619e6-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="619e6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="619e6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="619e6-146">-WhatIf</span></span>
<span data-ttu-id="619e6-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="619e6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="619e6-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="619e6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="619e6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619e6-149">CommonParameters</span></span>
<span data-ttu-id="619e6-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="619e6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619e6-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="619e6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619e6-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="619e6-152">INPUTS</span></span>

### <span data-ttu-id="619e6-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="619e6-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="619e6-154">System.String</span><span class="sxs-lookup"><span data-stu-id="619e6-154">System.String</span></span>

## <span data-ttu-id="619e6-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="619e6-155">OUTPUTS</span></span>

### <span data-ttu-id="619e6-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="619e6-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="619e6-157">Notas</span><span class="sxs-lookup"><span data-stu-id="619e6-157">NOTES</span></span>

## <span data-ttu-id="619e6-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="619e6-158">RELATED LINKS</span></span>
