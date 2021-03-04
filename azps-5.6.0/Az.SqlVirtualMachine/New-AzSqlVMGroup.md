---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: bc9c881a69ee2365dcb9ff805c1c14fe3f1bbf79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888644"
---
# <span data-ttu-id="0b845-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="0b845-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="0b845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b845-102">SYNOPSIS</span></span>
<span data-ttu-id="0b845-103">Cria um novo grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="0b845-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="0b845-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0b845-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b845-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b845-105">DESCRIPTION</span></span>
<span data-ttu-id="0b845-106">O cmdlet New-AzSqlVMGroup cria um grupo de máquinas SQL virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b845-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="0b845-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b845-107">EXAMPLES</span></span>

### <span data-ttu-id="0b845-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b845-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="0b845-109">Cria um novo grupo de máquinas virtuais do Azure SQL com vm de grupo de teste no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0b845-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="0b845-110">$profile é um objeto do tipo Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="0b845-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="0b845-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0b845-111">PARAMETERS</span></span>

### <span data-ttu-id="0b845-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b845-112">-AsJob</span></span>
<span data-ttu-id="0b845-113">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0b845-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0b845-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="0b845-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="0b845-115">Nome usado para criar cluster</span><span class="sxs-lookup"><span data-stu-id="0b845-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="0b845-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="0b845-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="0b845-117">Nome usado para cluster operacional</span><span class="sxs-lookup"><span data-stu-id="0b845-117">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b845-118">-DefaultProfile</span></span>
<span data-ttu-id="0b845-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b845-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b845-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="0b845-120">-DomainFqdn</span></span>
<span data-ttu-id="0b845-121">Nome totalmente qualificado do domínio</span><span class="sxs-lookup"><span data-stu-id="0b845-121">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="0b845-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="0b845-123">Caminho opcional para testemunha de compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="0b845-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="0b845-124">-Location</span><span class="sxs-lookup"><span data-stu-id="0b845-124">-Location</span></span>
<span data-ttu-id="0b845-125">SQL local do grupo de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="0b845-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0b845-126">-Name</span></span>
<span data-ttu-id="0b845-127">SQL nome do grupo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b845-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-128">-Offer</span><span class="sxs-lookup"><span data-stu-id="0b845-128">-Offer</span></span>
<span data-ttu-id="0b845-129">SQL de grupo de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="0b845-129">SQL virtual machine group offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="0b845-130">-OuPath</span></span>
<span data-ttu-id="0b845-131">Caminho da Unidade Organizacional no qual os nós e o cluster estarão presentes</span><span class="sxs-lookup"><span data-stu-id="0b845-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="0b845-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b845-132">-ResourceGroupName</span></span>
<span data-ttu-id="0b845-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b845-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="0b845-134">-Sku</span></span>
<span data-ttu-id="0b845-135">SQL tipo de edição do grupo de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="0b845-135">SQL virtual machine group edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="0b845-136">-SqlServiceAccount</span></span>
<span data-ttu-id="0b845-137">Nome em que SQL serviço será executado em todas as SQL virtuais participantes no cluster</span><span class="sxs-lookup"><span data-stu-id="0b845-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0b845-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="0b845-139">Chave primária da conta de armazenamento testemunha</span><span class="sxs-lookup"><span data-stu-id="0b845-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="0b845-140">-StorageAccountUrl</span></span>
<span data-ttu-id="0b845-141">Chave primária da conta de armazenamento testemunha</span><span class="sxs-lookup"><span data-stu-id="0b845-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b845-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b845-142">-Tag</span></span>
<span data-ttu-id="0b845-143">As marcas a associar ao grupo SQL máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b845-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="0b845-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b845-144">-Confirm</span></span>
<span data-ttu-id="0b845-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b845-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b845-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b845-146">-WhatIf</span></span>
<span data-ttu-id="0b845-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b845-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b845-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b845-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b845-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b845-149">CommonParameters</span></span>
<span data-ttu-id="0b845-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b845-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b845-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b845-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b845-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b845-152">INPUTS</span></span>

### <span data-ttu-id="0b845-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0b845-153">System.String</span></span>

## <span data-ttu-id="0b845-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0b845-154">OUTPUTS</span></span>

### <span data-ttu-id="0b845-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="0b845-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="0b845-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="0b845-156">NOTES</span></span>

## <span data-ttu-id="0b845-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b845-157">RELATED LINKS</span></span>
