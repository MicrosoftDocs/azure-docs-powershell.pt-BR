---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110941"
---
# <span data-ttu-id="4b862-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="4b862-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="4b862-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b862-102">SYNOPSIS</span></span>
<span data-ttu-id="4b862-103">Failovers de uma Instância Gerenciada do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b862-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="4b862-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b862-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b862-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b862-105">DESCRIPTION</span></span>
<span data-ttu-id="4b862-106">O cmdlet **Invoke-AzSqlInstanceFailover** failovers an Azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="4b862-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="4b862-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b862-107">EXAMPLES</span></span>

### <span data-ttu-id="4b862-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b862-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="4b862-109">Esse comando fará failover na réplica principal da instância chamada "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="4b862-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="4b862-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4b862-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="4b862-111">Esse comando falhará na replica secundária acessível da instância gerenciada "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="4b862-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="4b862-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b862-112">PARAMETERS</span></span>

### <span data-ttu-id="4b862-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b862-113">-AsJob</span></span>
<span data-ttu-id="4b862-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4b862-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b862-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b862-115">-DefaultProfile</span></span>
<span data-ttu-id="4b862-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b862-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b862-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4b862-117">-Force</span></span>
<span data-ttu-id="4b862-118">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="4b862-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4b862-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b862-119">-Name</span></span>
<span data-ttu-id="4b862-120">O nome da instância SQL do Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4b862-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="4b862-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b862-121">-PassThru</span></span>
<span data-ttu-id="4b862-122">Na execução bem-sucedida, retorna verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="4b862-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="4b862-123">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="4b862-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4b862-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="4b862-124">-ReadableSecondary</span></span>
<span data-ttu-id="4b862-125">Failover a replica secundária acessível em vez da réplica primária padrão</span><span class="sxs-lookup"><span data-stu-id="4b862-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="4b862-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b862-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b862-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b862-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4b862-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4b862-128">-Confirm</span></span>
<span data-ttu-id="4b862-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b862-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b862-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b862-130">-WhatIf</span></span>
<span data-ttu-id="4b862-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4b862-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b862-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b862-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b862-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b862-133">CommonParameters</span></span>
<span data-ttu-id="4b862-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b862-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b862-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b862-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b862-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b862-136">INPUTS</span></span>

### <span data-ttu-id="4b862-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4b862-137">System.String</span></span>

## <span data-ttu-id="4b862-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b862-138">OUTPUTS</span></span>

## <span data-ttu-id="4b862-139">Notas</span><span class="sxs-lookup"><span data-stu-id="4b862-139">NOTES</span></span>

## <span data-ttu-id="4b862-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b862-140">RELATED LINKS</span></span>
