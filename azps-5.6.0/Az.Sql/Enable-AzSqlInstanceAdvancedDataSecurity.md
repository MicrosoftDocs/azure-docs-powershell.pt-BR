---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 01effbfbd0a9f4df8cd8bf611c6a2f25875452a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885253"
---
# <span data-ttu-id="d7c9f-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="d7c9f-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="d7c9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c9f-103">Habilita a Segurança Avançada de Dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="d7c9f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d7c9f-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7c9f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d7c9f-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c9f-106">O cmdlet **Enable-AzSqlInstanceAdvancedDataSecurity** habilita a Segurança Avançada de Dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="d7c9f-107">A Segurança Avançada de Dados é um pacote de segurança unificado que inclui Classificação de Dados, Avaliação de Vulnerabilidade e Proteção Avançada contra Ameaças para sua instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="d7c9f-108">(Uma nova conta de armazenamento será criada automaticamente para salvar avaliações de vulnerabilidade.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="d7c9f-109">Se uma conta de armazenamento tiver sido criada anteriormente para essa finalidade, ela será usada em vez disso)</span><span class="sxs-lookup"><span data-stu-id="d7c9f-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="d7c9f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7c9f-110">EXAMPLES</span></span>

### <span data-ttu-id="d7c9f-111">Exemplo 1: Habilitar a instância gerenciada Segurança Avançada de Dados</span><span class="sxs-lookup"><span data-stu-id="d7c9f-111">Example 1: Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="d7c9f-112">Exemplo 2: Habilitar a segurança avançada de dados da instância gerenciada a partir do recurso de servidor</span><span class="sxs-lookup"><span data-stu-id="d7c9f-112">Example 2: Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="d7c9f-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d7c9f-113">Example 3</span></span>

<span data-ttu-id="d7c9f-114">Habilita a Segurança Avançada de Dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-114">Enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="d7c9f-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d7c9f-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Enable-AzSqlInstanceAdvancedDataSecurity -DoNotConfigureVulnerabilityAssessment -InstanceName 'ContosoManagedInstanceName' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="d7c9f-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d7c9f-116">PARAMETERS</span></span>

### <span data-ttu-id="d7c9f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7c9f-117">-AsJob</span></span>
<span data-ttu-id="d7c9f-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7c9f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7c9f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c9f-119">-DefaultProfile</span></span>
<span data-ttu-id="d7c9f-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7c9f-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d7c9f-121">-DeploymentName</span></span>
<span data-ttu-id="d7c9f-122">Fornecer um nome personalizado para implantação avançada de Segurança de Dados</span><span class="sxs-lookup"><span data-stu-id="d7c9f-122">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="d7c9f-123">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="d7c9f-123">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="d7c9f-124">Não habilitar automaticamente a Avaliação de Vulnerabilidade (Isso não criará uma conta de armazenamento)</span><span class="sxs-lookup"><span data-stu-id="d7c9f-124">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="d7c9f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7c9f-125">-InputObject</span></span>
<span data-ttu-id="d7c9f-126">O objeto de instância gerenciada a ser usado com a operação de política de Segurança de Dados Avançada</span><span class="sxs-lookup"><span data-stu-id="d7c9f-126">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c9f-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d7c9f-127">-InstanceName</span></span>
<span data-ttu-id="d7c9f-128">SQL nome da instância gerenciada do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-128">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c9f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c9f-129">-ResourceGroupName</span></span>
<span data-ttu-id="d7c9f-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c9f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7c9f-131">-Confirm</span></span>
<span data-ttu-id="d7c9f-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7c9f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7c9f-133">-WhatIf</span></span>
<span data-ttu-id="d7c9f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7c9f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7c9f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c9f-136">CommonParameters</span></span>
<span data-ttu-id="d7c9f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c9f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c9f-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7c9f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c9f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7c9f-139">INPUTS</span></span>

### <span data-ttu-id="d7c9f-140">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d7c9f-140">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d7c9f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d7c9f-141">System.String</span></span>

## <span data-ttu-id="d7c9f-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d7c9f-142">OUTPUTS</span></span>

### <span data-ttu-id="d7c9f-143">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d7c9f-143">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="d7c9f-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="d7c9f-144">NOTES</span></span>

## <span data-ttu-id="d7c9f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7c9f-145">RELATED LINKS</span></span>
