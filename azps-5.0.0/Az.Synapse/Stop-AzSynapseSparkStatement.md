---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125224"
---
# <span data-ttu-id="8bf4e-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="8bf4e-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="8bf4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bf4e-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf4e-103">Cancela uma declaração de Synapse analítico da análise.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="8bf4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bf4e-104">SYNTAX</span></span>

### <span data-ttu-id="8bf4e-105">StopSparkStatementByIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8bf4e-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bf4e-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bf4e-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bf4e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bf4e-107">DESCRIPTION</span></span>
<span data-ttu-id="8bf4e-108">O cmdlet **Stop-AzSynapseSparkStatement** cancela uma declaração Analytics do Synapse.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="8bf4e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bf4e-109">EXAMPLES</span></span>

### <span data-ttu-id="8bf4e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bf4e-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="8bf4e-111">Esse comando cancela a instrução do Spark com a ID Livy especificada.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="8bf4e-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8bf4e-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="8bf4e-113">Esse comando cancela a instrução do Spark com a ID Livy especificada por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="8bf4e-114">OS</span><span class="sxs-lookup"><span data-stu-id="8bf4e-114">PARAMETERS</span></span>

### <span data-ttu-id="8bf4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf4e-115">-DefaultProfile</span></span>
<span data-ttu-id="8bf4e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf4e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8bf4e-117">-Force</span></span>
<span data-ttu-id="8bf4e-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8bf4e-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="8bf4e-119">-LivyId</span></span>
<span data-ttu-id="8bf4e-120">Identificador da instrução Spark.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf4e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bf4e-121">-PassThru</span></span>
<span data-ttu-id="8bf4e-122">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8bf4e-123">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8bf4e-124">-Identificação_da_sessão</span><span class="sxs-lookup"><span data-stu-id="8bf4e-124">-SessionId</span></span>
<span data-ttu-id="8bf4e-125">Identificador da sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf4e-126">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="8bf4e-126">-SessionObject</span></span>
<span data-ttu-id="8bf4e-127">Objeto de entrada de sessão do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bf4e-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8bf4e-128">-SparkPoolName</span></span>
<span data-ttu-id="8bf4e-129">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf4e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8bf4e-130">-WorkspaceName</span></span>
<span data-ttu-id="8bf4e-131">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf4e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bf4e-132">-Confirm</span></span>
<span data-ttu-id="8bf4e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bf4e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf4e-134">-WhatIf</span></span>
<span data-ttu-id="8bf4e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf4e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bf4e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf4e-137">CommonParameters</span></span>
<span data-ttu-id="8bf4e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf4e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf4e-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bf4e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf4e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bf4e-140">INPUTS</span></span>

### <span data-ttu-id="8bf4e-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8bf4e-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="8bf4e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bf4e-142">OUTPUTS</span></span>

### <span data-ttu-id="8bf4e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bf4e-143">System.Boolean</span></span>

## <span data-ttu-id="8bf4e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bf4e-144">NOTES</span></span>

## <span data-ttu-id="8bf4e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bf4e-145">RELATED LINKS</span></span>
