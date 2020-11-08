---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111350"
---
# <span data-ttu-id="361c6-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="361c6-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="361c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="361c6-102">SYNOPSIS</span></span>
<span data-ttu-id="361c6-103">Failover de uma instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="361c6-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="361c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="361c6-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="361c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="361c6-105">DESCRIPTION</span></span>
<span data-ttu-id="361c6-106">O cmdlet **Invoke-AzSqlInstanceFailover** failoveru uma instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="361c6-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="361c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="361c6-107">EXAMPLES</span></span>

### <span data-ttu-id="361c6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="361c6-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="361c6-109">Esse comando irá failover na réplica primária da instância chamada "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="361c6-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="361c6-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="361c6-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="361c6-111">Esse comando fará o failover da réplica secundária legível da instância gerenciada "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="361c6-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="361c6-112">OS</span><span class="sxs-lookup"><span data-stu-id="361c6-112">PARAMETERS</span></span>

### <span data-ttu-id="361c6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="361c6-113">-AsJob</span></span>
<span data-ttu-id="361c6-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="361c6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="361c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361c6-115">-DefaultProfile</span></span>
<span data-ttu-id="361c6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="361c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="361c6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="361c6-117">-Force</span></span>
<span data-ttu-id="361c6-118">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="361c6-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="361c6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="361c6-119">-Name</span></span>
<span data-ttu-id="361c6-120">O nome da instância do Azure SQL a ser removida.</span><span class="sxs-lookup"><span data-stu-id="361c6-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="361c6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="361c6-121">-PassThru</span></span>
<span data-ttu-id="361c6-122">Na execução bem-sucedida, retorna verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="361c6-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="361c6-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="361c6-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="361c6-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="361c6-124">-ReadableSecondary</span></span>
<span data-ttu-id="361c6-125">Failover da réplica secundária legível em vez da réplica primária padrão</span><span class="sxs-lookup"><span data-stu-id="361c6-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="361c6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="361c6-126">-ResourceGroupName</span></span>
<span data-ttu-id="361c6-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="361c6-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="361c6-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="361c6-128">-Confirm</span></span>
<span data-ttu-id="361c6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="361c6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="361c6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="361c6-130">-WhatIf</span></span>
<span data-ttu-id="361c6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="361c6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="361c6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="361c6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="361c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361c6-133">CommonParameters</span></span>
<span data-ttu-id="361c6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361c6-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="361c6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361c6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="361c6-136">INPUTS</span></span>

### <span data-ttu-id="361c6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="361c6-137">System.String</span></span>

## <span data-ttu-id="361c6-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="361c6-138">OUTPUTS</span></span>

## <span data-ttu-id="361c6-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="361c6-139">NOTES</span></span>

## <span data-ttu-id="361c6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="361c6-140">RELATED LINKS</span></span>
