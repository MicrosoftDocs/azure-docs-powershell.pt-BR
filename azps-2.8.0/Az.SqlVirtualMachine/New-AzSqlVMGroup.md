---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: e46df689b4cc6953f29f5361c4df8bc5bd878acd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773967"
---
# <span data-ttu-id="428f1-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="428f1-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="428f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="428f1-102">SYNOPSIS</span></span>
<span data-ttu-id="428f1-103">Cria um novo grupo de máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="428f1-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="428f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="428f1-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="428f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="428f1-105">DESCRIPTION</span></span>
<span data-ttu-id="428f1-106">O cmdlet New-AzSqlVMGroup cria um grupo de máquina virtual do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="428f1-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="428f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="428f1-107">EXAMPLES</span></span>

### <span data-ttu-id="428f1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="428f1-108">Example 1</span></span>
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

<span data-ttu-id="428f1-109">Cria um novo grupo de máquinas virtuais do Azure SQL com VM de grupo de teste na ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="428f1-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="428f1-110">$profile é um objeto do tipo Microsoft. Azure. Management. SqlVirtualMachine. Models. WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="428f1-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="428f1-111">OS</span><span class="sxs-lookup"><span data-stu-id="428f1-111">PARAMETERS</span></span>

### <span data-ttu-id="428f1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="428f1-112">-AsJob</span></span>
<span data-ttu-id="428f1-113">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="428f1-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="428f1-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="428f1-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="428f1-115">Nome usado para a criação de um cluster</span><span class="sxs-lookup"><span data-stu-id="428f1-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="428f1-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="428f1-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="428f1-117">Nome usado para o cluster operacional</span><span class="sxs-lookup"><span data-stu-id="428f1-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="428f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428f1-118">-DefaultProfile</span></span>
<span data-ttu-id="428f1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="428f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428f1-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="428f1-120">-DomainFqdn</span></span>
<span data-ttu-id="428f1-121">Nome totalmente qualificado do domínio</span><span class="sxs-lookup"><span data-stu-id="428f1-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="428f1-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="428f1-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="428f1-123">Caminho opcional para testemunha do FileShare</span><span class="sxs-lookup"><span data-stu-id="428f1-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="428f1-124">-Local</span><span class="sxs-lookup"><span data-stu-id="428f1-124">-Location</span></span>
<span data-ttu-id="428f1-125">Local do grupo de máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="428f1-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="428f1-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="428f1-126">-Name</span></span>
<span data-ttu-id="428f1-127">Nome do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="428f1-127">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="428f1-128">-Oferta</span><span class="sxs-lookup"><span data-stu-id="428f1-128">-Offer</span></span>
<span data-ttu-id="428f1-129">Oferta de grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="428f1-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="428f1-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="428f1-130">-OuPath</span></span>
<span data-ttu-id="428f1-131">Caminho da unidade organizacional em que os nós e o cluster estarão presentes</span><span class="sxs-lookup"><span data-stu-id="428f1-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="428f1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="428f1-132">-ResourceGroupName</span></span>
<span data-ttu-id="428f1-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="428f1-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="428f1-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="428f1-134">-Sku</span></span>
<span data-ttu-id="428f1-135">Tipo da edição de grupo da máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="428f1-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="428f1-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="428f1-136">-SqlServiceAccount</span></span>
<span data-ttu-id="428f1-137">Nome em que o serviço SQL será executado em todas as máquinas virtuais do SQL no cluster</span><span class="sxs-lookup"><span data-stu-id="428f1-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="428f1-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="428f1-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="428f1-139">Chave primária da conta de armazenamento de testemunha</span><span class="sxs-lookup"><span data-stu-id="428f1-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="428f1-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="428f1-140">-StorageAccountUrl</span></span>
<span data-ttu-id="428f1-141">Chave primária da conta de armazenamento de testemunha</span><span class="sxs-lookup"><span data-stu-id="428f1-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="428f1-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="428f1-142">-Tag</span></span>
<span data-ttu-id="428f1-143">As marcas a serem associadas ao grupo da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="428f1-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="428f1-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="428f1-144">-Confirm</span></span>
<span data-ttu-id="428f1-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="428f1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="428f1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="428f1-146">-WhatIf</span></span>
<span data-ttu-id="428f1-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="428f1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="428f1-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="428f1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="428f1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428f1-149">CommonParameters</span></span>
<span data-ttu-id="428f1-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="428f1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428f1-151">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="428f1-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428f1-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="428f1-152">INPUTS</span></span>

### <span data-ttu-id="428f1-153">System. String</span><span class="sxs-lookup"><span data-stu-id="428f1-153">System.String</span></span>

## <span data-ttu-id="428f1-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="428f1-154">OUTPUTS</span></span>

### <span data-ttu-id="428f1-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="428f1-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="428f1-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="428f1-156">NOTES</span></span>

## <span data-ttu-id="428f1-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="428f1-157">RELATED LINKS</span></span>