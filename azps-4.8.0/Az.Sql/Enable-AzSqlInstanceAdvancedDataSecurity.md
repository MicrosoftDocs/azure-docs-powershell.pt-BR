---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 03f393daf629329ff90a6606760a0c7bc70ad788
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113927"
---
# <span data-ttu-id="22b1e-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="22b1e-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="22b1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="22b1e-103">Habilita a segurança avançada de dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="22b1e-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="22b1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22b1e-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22b1e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="22b1e-106">O cmdlet **Enable-AzSqlInstanceAdvancedDataSecurity** habilita a segurança avançada de dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="22b1e-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="22b1e-107">A segurança avançada de dados é um pacote de segurança unificado que inclui classificação de dados, avaliação de vulnerabilidade e proteção avançada contra ameaças para sua instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="22b1e-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="22b1e-108">(Uma nova conta de armazenamento será criada automaticamente para salvar avaliações de vulnerabilidade.</span><span class="sxs-lookup"><span data-stu-id="22b1e-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="22b1e-109">Se uma conta de armazenamento foi criada anteriormente para essa finalidade, ela será usada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="22b1e-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="22b1e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22b1e-110">EXAMPLES</span></span>

### <span data-ttu-id="22b1e-111">Exemplo 1: habilitar a instância gerenciada segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="22b1e-111">Example 1: Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="22b1e-112">Exemplo 2: habilitar a instância gerenciada segurança de dados avançada do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="22b1e-112">Example 2: Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="22b1e-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="22b1e-113">Example 3</span></span>

<span data-ttu-id="22b1e-114">Habilita a segurança avançada de dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="22b1e-114">Enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="22b1e-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="22b1e-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Enable-AzSqlInstanceAdvancedDataSecurity -DoNotConfigureVulnerabilityAssessment -InstanceName 'ContosoManagedInstanceName' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="22b1e-116">OS</span><span class="sxs-lookup"><span data-stu-id="22b1e-116">PARAMETERS</span></span>

### <span data-ttu-id="22b1e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22b1e-117">-AsJob</span></span>
<span data-ttu-id="22b1e-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="22b1e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22b1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b1e-119">-DefaultProfile</span></span>
<span data-ttu-id="22b1e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22b1e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b1e-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="22b1e-121">-DeploymentName</span></span>
<span data-ttu-id="22b1e-122">Fornecer um nome personalizado para a implantação de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="22b1e-122">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="22b1e-123">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="22b1e-123">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="22b1e-124">Não habilitar a avaliação de vulnerabilidade automaticamente (isso não criará uma conta de armazenamento)</span><span class="sxs-lookup"><span data-stu-id="22b1e-124">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="22b1e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22b1e-125">-InputObject</span></span>
<span data-ttu-id="22b1e-126">O objeto de instância gerenciado a ser usado com a operação de política de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="22b1e-126">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="22b1e-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="22b1e-127">-InstanceName</span></span>
<span data-ttu-id="22b1e-128">Nome da instância gerenciada do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="22b1e-128">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="22b1e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b1e-129">-ResourceGroupName</span></span>
<span data-ttu-id="22b1e-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22b1e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="22b1e-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22b1e-131">-Confirm</span></span>
<span data-ttu-id="22b1e-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22b1e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b1e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b1e-133">-WhatIf</span></span>
<span data-ttu-id="22b1e-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22b1e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b1e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22b1e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b1e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b1e-136">CommonParameters</span></span>
<span data-ttu-id="22b1e-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b1e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b1e-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22b1e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b1e-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22b1e-139">INPUTS</span></span>

### <span data-ttu-id="22b1e-140">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="22b1e-140">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="22b1e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="22b1e-141">System.String</span></span>

## <span data-ttu-id="22b1e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22b1e-142">OUTPUTS</span></span>

### <span data-ttu-id="22b1e-143">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="22b1e-143">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="22b1e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22b1e-144">NOTES</span></span>

## <span data-ttu-id="22b1e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22b1e-145">RELATED LINKS</span></span>
