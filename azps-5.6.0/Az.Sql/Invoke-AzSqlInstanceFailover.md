---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: cde8f48ebef73e3669a82f05c2ba91a4a4e4c582
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888072"
---
# <span data-ttu-id="a64cc-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="a64cc-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="a64cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a64cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a64cc-103">Failovers an Azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="a64cc-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="a64cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a64cc-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a64cc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a64cc-105">DESCRIPTION</span></span>
<span data-ttu-id="a64cc-106">O cmdlet **Invoke-AzSqlInstanceFailover** failovers an Azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="a64cc-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="a64cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a64cc-107">EXAMPLES</span></span>

### <span data-ttu-id="a64cc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a64cc-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="a64cc-109">Este comando fará failover da réplica primária da instância chamada "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="a64cc-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="a64cc-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a64cc-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="a64cc-111">Este comando fará failover da réplica secundária acessível da instância gerenciada "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="a64cc-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="a64cc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a64cc-112">PARAMETERS</span></span>

### <span data-ttu-id="a64cc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a64cc-113">-AsJob</span></span>
<span data-ttu-id="a64cc-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a64cc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a64cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a64cc-115">-DefaultProfile</span></span>
<span data-ttu-id="a64cc-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a64cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a64cc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a64cc-117">-Force</span></span>
<span data-ttu-id="a64cc-118">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="a64cc-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a64cc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a64cc-119">-Name</span></span>
<span data-ttu-id="a64cc-120">O nome da instância de SQL do Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a64cc-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a64cc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a64cc-121">-PassThru</span></span>
<span data-ttu-id="a64cc-122">Em Execução bem-sucedida, retorna true.</span><span class="sxs-lookup"><span data-stu-id="a64cc-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="a64cc-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a64cc-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a64cc-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="a64cc-124">-ReadableSecondary</span></span>
<span data-ttu-id="a64cc-125">Failover da réplica secundária acessível em vez da réplica primária padrão</span><span class="sxs-lookup"><span data-stu-id="a64cc-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="a64cc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a64cc-126">-ResourceGroupName</span></span>
<span data-ttu-id="a64cc-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a64cc-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a64cc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a64cc-128">-Confirm</span></span>
<span data-ttu-id="a64cc-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a64cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a64cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a64cc-130">-WhatIf</span></span>
<span data-ttu-id="a64cc-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a64cc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a64cc-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a64cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a64cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a64cc-133">CommonParameters</span></span>
<span data-ttu-id="a64cc-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a64cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a64cc-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a64cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a64cc-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a64cc-136">INPUTS</span></span>

### <span data-ttu-id="a64cc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a64cc-137">System.String</span></span>

## <span data-ttu-id="a64cc-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a64cc-138">OUTPUTS</span></span>

## <span data-ttu-id="a64cc-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="a64cc-139">NOTES</span></span>

## <span data-ttu-id="a64cc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a64cc-140">RELATED LINKS</span></span>
