---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: b3e3aa1414b24324278f4191fd53a28a75d0cfab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773709"
---
# <span data-ttu-id="9ff14-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="9ff14-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="9ff14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ff14-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff14-103">Atualiza uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="9ff14-103">Updates a job credential</span></span>

## <span data-ttu-id="9ff14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ff14-104">SYNTAX</span></span>

### <span data-ttu-id="9ff14-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ff14-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ff14-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ff14-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ff14-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="9ff14-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff14-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ff14-108">DESCRIPTION</span></span>
<span data-ttu-id="9ff14-109">O cmdlet Set-AzSqlElasticJobCredential atualiza uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="9ff14-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="9ff14-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ff14-110">EXAMPLES</span></span>

### <span data-ttu-id="9ff14-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ff14-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="9ff14-112">Atualiza uma credencial de trabalho</span><span class="sxs-lookup"><span data-stu-id="9ff14-112">Updates a job credential</span></span>

## <span data-ttu-id="9ff14-113">OS</span><span class="sxs-lookup"><span data-stu-id="9ff14-113">PARAMETERS</span></span>

### <span data-ttu-id="9ff14-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9ff14-114">-AgentName</span></span>
<span data-ttu-id="9ff14-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="9ff14-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="9ff14-116">-Credential</span></span>
<span data-ttu-id="9ff14-117">A credencial</span><span class="sxs-lookup"><span data-stu-id="9ff14-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff14-118">-DefaultProfile</span></span>
<span data-ttu-id="9ff14-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff14-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff14-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ff14-120">-InputObject</span></span>
<span data-ttu-id="9ff14-121">O objeto de credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="9ff14-121">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ff14-122">-Name</span></span>
<span data-ttu-id="9ff14-123">O nome da credencial do trabalho</span><span class="sxs-lookup"><span data-stu-id="9ff14-123">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff14-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ff14-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9ff14-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ff14-126">-ResourceId</span></span>
<span data-ttu-id="9ff14-127">A ID do recurso de credenciais do trabalho</span><span class="sxs-lookup"><span data-stu-id="9ff14-127">The job credential resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="9ff14-128">-ServerName</span></span>
<span data-ttu-id="9ff14-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="9ff14-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ff14-130">-Confirm</span></span>
<span data-ttu-id="9ff14-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff14-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff14-132">-WhatIf</span></span>
<span data-ttu-id="9ff14-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ff14-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff14-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ff14-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff14-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff14-135">CommonParameters</span></span>
<span data-ttu-id="9ff14-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff14-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff14-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff14-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff14-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ff14-138">INPUTS</span></span>

### <span data-ttu-id="9ff14-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9ff14-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="9ff14-140">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="9ff14-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9ff14-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ff14-141">OUTPUTS</span></span>

### <span data-ttu-id="9ff14-142">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="9ff14-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9ff14-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ff14-143">NOTES</span></span>

## <span data-ttu-id="9ff14-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ff14-144">RELATED LINKS</span></span>