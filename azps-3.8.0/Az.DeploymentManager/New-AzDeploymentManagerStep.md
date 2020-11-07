---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944403"
---
# <span data-ttu-id="2e868-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="2e868-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="2e868-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e868-102">SYNOPSIS</span></span>
<span data-ttu-id="2e868-103">Cria uma etapa.</span><span class="sxs-lookup"><span data-stu-id="2e868-103">Creates a step.</span></span>

## <span data-ttu-id="2e868-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e868-104">SYNTAX</span></span>

### <span data-ttu-id="2e868-105">Aguardar (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e868-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e868-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="2e868-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e868-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="2e868-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e868-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e868-108">DESCRIPTION</span></span>
<span data-ttu-id="2e868-109">O cmdlet **New-AzDeploymentManagerStep** cria uma etapa de implantação que pode ser referenciada em implementações.</span><span class="sxs-lookup"><span data-stu-id="2e868-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="2e868-110">Especifique o *nome* , *ResourceGroupName* e propriedades necessárias.</span><span class="sxs-lookup"><span data-stu-id="2e868-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="2e868-111">Você pode modificar o objeto retornado localmente e, em seguida, aplicar as alterações à etapa usando o cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="2e868-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="2e868-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e868-112">EXAMPLES</span></span>

### <span data-ttu-id="2e868-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e868-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="2e868-114">Cria uma etapa no ContosoResourceGroup com o nome ContosoService1WaitStep no centro dos EUA como o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2e868-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="2e868-115">A Propriedade Duration fornece a duração que a distribuição aguardará antes de executar a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="2e868-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="2e868-116">OS</span><span class="sxs-lookup"><span data-stu-id="2e868-116">PARAMETERS</span></span>

### <span data-ttu-id="2e868-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e868-117">-DefaultProfile</span></span>
<span data-ttu-id="2e868-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e868-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e868-119">-Duração</span><span class="sxs-lookup"><span data-stu-id="2e868-119">-Duration</span></span>
<span data-ttu-id="2e868-120">A duração a ser esperada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="2e868-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="2e868-121">Por exemplo: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="2e868-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e868-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="2e868-122">-HealthCheckProperties</span></span>
<span data-ttu-id="2e868-123">As propriedades da verificação de integridade.</span><span class="sxs-lookup"><span data-stu-id="2e868-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e868-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="2e868-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="2e868-125">O caminho para o arquivo onde as propriedades da verificação de integridade são definidas.</span><span class="sxs-lookup"><span data-stu-id="2e868-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e868-126">-Local</span><span class="sxs-lookup"><span data-stu-id="2e868-126">-Location</span></span>
<span data-ttu-id="2e868-127">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2e868-127">The location of the resource.</span></span>

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

### <span data-ttu-id="2e868-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e868-128">-Name</span></span>
<span data-ttu-id="2e868-129">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="2e868-129">The name of the step.</span></span>

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

### <span data-ttu-id="2e868-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e868-130">-ResourceGroupName</span></span>
<span data-ttu-id="2e868-131">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e868-131">The resource group.</span></span>

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

### <span data-ttu-id="2e868-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="2e868-132">-Tag</span></span>
<span data-ttu-id="2e868-133">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e868-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="2e868-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e868-134">-Confirm</span></span>
<span data-ttu-id="2e868-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e868-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e868-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e868-136">-WhatIf</span></span>
<span data-ttu-id="2e868-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e868-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e868-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e868-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e868-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e868-139">CommonParameters</span></span>
<span data-ttu-id="2e868-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e868-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e868-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e868-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e868-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e868-142">INPUTS</span></span>

### <span data-ttu-id="2e868-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e868-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e868-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e868-144">OUTPUTS</span></span>

### <span data-ttu-id="2e868-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="2e868-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="2e868-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e868-146">NOTES</span></span>

## <span data-ttu-id="2e868-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e868-147">RELATED LINKS</span></span>
