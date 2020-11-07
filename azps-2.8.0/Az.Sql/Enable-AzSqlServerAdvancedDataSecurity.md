---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: c2c3b634eb5a9e031c375a6cc696298becd58e8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773496"
---
# <span data-ttu-id="48739-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="48739-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="48739-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48739-102">SYNOPSIS</span></span>
<span data-ttu-id="48739-103">Habilita a segurança avançada de dados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="48739-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="48739-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48739-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48739-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48739-105">DESCRIPTION</span></span>
<span data-ttu-id="48739-106">O cmdlet **Enable-AzSqlServerAdvancedDataSecurity** permite a segurança avançada de dados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="48739-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="48739-107">A segurança avançada de dados é um pacote de segurança unificado que inclui classificação de dados, avaliação de vulnerabilidade e proteção avançada contra ameaças para o seu servidor.</span><span class="sxs-lookup"><span data-stu-id="48739-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="48739-108">(Uma nova conta de armazenamento será criada automaticamente para salvar avaliações de vulnerabilidade.</span><span class="sxs-lookup"><span data-stu-id="48739-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="48739-109">Se uma conta de armazenamento foi criada anteriormente para essa finalidade, ela será usada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="48739-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="48739-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48739-110">EXAMPLES</span></span>

### <span data-ttu-id="48739-111">Exemplo 1-habilitar a segurança de dados avançados do servidor</span><span class="sxs-lookup"><span data-stu-id="48739-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="48739-112">Exemplo 2-habilitar a segurança de dados avançados do servidor do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="48739-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="48739-113">OS</span><span class="sxs-lookup"><span data-stu-id="48739-113">PARAMETERS</span></span>

### <span data-ttu-id="48739-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48739-114">-AsJob</span></span>
<span data-ttu-id="48739-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="48739-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48739-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48739-116">-DefaultProfile</span></span>
<span data-ttu-id="48739-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48739-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48739-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="48739-118">-DeploymentName</span></span>
<span data-ttu-id="48739-119">Fornecer um nome personalizado para a implantação de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="48739-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="48739-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="48739-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="48739-121">Não habilitar a avaliação de vulnerabilidade automaticamente (isso não criará uma conta de armazenamento)</span><span class="sxs-lookup"><span data-stu-id="48739-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="48739-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48739-122">-InputObject</span></span>
<span data-ttu-id="48739-123">O objeto de servidor a ser usado com a operação de política de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="48739-123">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48739-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48739-124">-ResourceGroupName</span></span>
<span data-ttu-id="48739-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48739-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="48739-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="48739-126">-ServerName</span></span>
<span data-ttu-id="48739-127">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="48739-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="48739-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48739-128">-Confirm</span></span>
<span data-ttu-id="48739-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48739-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48739-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48739-130">-WhatIf</span></span>
<span data-ttu-id="48739-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48739-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48739-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48739-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48739-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48739-133">CommonParameters</span></span>
<span data-ttu-id="48739-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48739-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48739-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48739-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48739-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48739-136">INPUTS</span></span>

### <span data-ttu-id="48739-137">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="48739-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="48739-138">System. String</span><span class="sxs-lookup"><span data-stu-id="48739-138">System.String</span></span>

## <span data-ttu-id="48739-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48739-139">OUTPUTS</span></span>

### <span data-ttu-id="48739-140">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="48739-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="48739-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48739-141">NOTES</span></span>

## <span data-ttu-id="48739-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48739-142">RELATED LINKS</span></span>