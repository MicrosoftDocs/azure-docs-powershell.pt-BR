---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113840"
---
# <span data-ttu-id="b0f0e-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="b0f0e-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="b0f0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f0e-103">Atualiza um grupo da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="b0f0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0f0e-104">SYNTAX</span></span>

### <span data-ttu-id="b0f0e-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0f0e-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0f0e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b0f0e-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0f0e-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="b0f0e-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0f0e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0f0e-108">DESCRIPTION</span></span>
<span data-ttu-id="b0f0e-109">O cmdlet Update-AzSqlVMGroup atualiza um grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="b0f0e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0f0e-110">EXAMPLES</span></span>

### <span data-ttu-id="b0f0e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b0f0e-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="b0f0e-112">Atualiza as marcas de um grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="b0f0e-113">OS</span><span class="sxs-lookup"><span data-stu-id="b0f0e-113">PARAMETERS</span></span>

### <span data-ttu-id="b0f0e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0f0e-114">-AsJob</span></span>
<span data-ttu-id="b0f0e-115">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b0f0e-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="b0f0e-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="b0f0e-117">Nome usado para a criação de um cluster</span><span class="sxs-lookup"><span data-stu-id="b0f0e-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="b0f0e-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="b0f0e-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="b0f0e-119">Nome usado para o cluster operacional</span><span class="sxs-lookup"><span data-stu-id="b0f0e-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="b0f0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f0e-120">-DefaultProfile</span></span>
<span data-ttu-id="b0f0e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f0e-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="b0f0e-122">-DomainFqdn</span></span>
<span data-ttu-id="b0f0e-123">Nome totalmente qualificado do domínio</span><span class="sxs-lookup"><span data-stu-id="b0f0e-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="b0f0e-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="b0f0e-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="b0f0e-125">Caminho opcional para testemunha do FileShare</span><span class="sxs-lookup"><span data-stu-id="b0f0e-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="b0f0e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0f0e-126">-InputObject</span></span>
<span data-ttu-id="b0f0e-127">Objeto da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="b0f0e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0f0e-128">-Name</span></span>
<span data-ttu-id="b0f0e-129">Nome do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="b0f0e-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="b0f0e-130">-OuPath</span></span>
<span data-ttu-id="b0f0e-131">Caminho da unidade organizacional em que os nós e o cluster estarão presentes</span><span class="sxs-lookup"><span data-stu-id="b0f0e-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="b0f0e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f0e-132">-ResourceGroupName</span></span>
<span data-ttu-id="b0f0e-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="b0f0e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0f0e-134">-ResourceId</span></span>
<span data-ttu-id="b0f0e-135">ID do recurso de grupo da máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="b0f0e-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="b0f0e-136">-SqlServiceAccount</span></span>
<span data-ttu-id="b0f0e-137">Nome em que o serviço SQL será executado em todas as máquinas virtuais do SQL no cluster</span><span class="sxs-lookup"><span data-stu-id="b0f0e-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="b0f0e-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b0f0e-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="b0f0e-139">Chave primária da conta de armazenamento de testemunha</span><span class="sxs-lookup"><span data-stu-id="b0f0e-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="b0f0e-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b0f0e-140">-StorageAccountUrl</span></span>
<span data-ttu-id="b0f0e-141">Chave primária da conta de armazenamento de testemunha</span><span class="sxs-lookup"><span data-stu-id="b0f0e-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="b0f0e-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="b0f0e-142">-Tag</span></span>
<span data-ttu-id="b0f0e-143">As marcas a serem associadas ao grupo da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="b0f0e-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0f0e-144">-Confirm</span></span>
<span data-ttu-id="b0f0e-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f0e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f0e-146">-WhatIf</span></span>
<span data-ttu-id="b0f0e-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f0e-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f0e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f0e-149">CommonParameters</span></span>
<span data-ttu-id="b0f0e-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f0e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f0e-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0f0e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f0e-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0f0e-152">INPUTS</span></span>

### <span data-ttu-id="b0f0e-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b0f0e-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="b0f0e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b0f0e-154">System.String</span></span>

## <span data-ttu-id="b0f0e-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0f0e-155">OUTPUTS</span></span>

### <span data-ttu-id="b0f0e-156">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b0f0e-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b0f0e-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0f0e-157">NOTES</span></span>

## <span data-ttu-id="b0f0e-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0f0e-158">RELATED LINKS</span></span>
