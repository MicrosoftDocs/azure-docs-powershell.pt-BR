---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115764"
---
# <span data-ttu-id="e5542-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="e5542-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="e5542-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5542-102">SYNOPSIS</span></span>
<span data-ttu-id="e5542-103">Desabilita a Segurança Avançada de Dados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="e5542-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="e5542-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5542-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5542-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5542-105">DESCRIPTION</span></span>
<span data-ttu-id="e5542-106">O cmdlet **Disable-AzSqlServerAdvancedDataSecurity** desabilita a Segurança De Dados Avançada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="e5542-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="e5542-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5542-107">EXAMPLES</span></span>

### <span data-ttu-id="e5542-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5542-108">Example 1</span></span>
### <span data-ttu-id="e5542-109">Exemplo 2: Desabilitar a Segurança Avançada de Dados do servidor</span><span class="sxs-lookup"><span data-stu-id="e5542-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="e5542-110">Exemplo 3: Desabilitar a Segurança Avançada de Dados do servidor a partir do recurso de servidor</span><span class="sxs-lookup"><span data-stu-id="e5542-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="e5542-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5542-111">PARAMETERS</span></span>

### <span data-ttu-id="e5542-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5542-112">-DefaultProfile</span></span>
<span data-ttu-id="e5542-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5542-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5542-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5542-114">-InputObject</span></span>
<span data-ttu-id="e5542-115">O objeto do servidor a ser usado com a operação de política de Segurança de Dados Avançada</span><span class="sxs-lookup"><span data-stu-id="e5542-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="e5542-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5542-116">-ResourceGroupName</span></span>
<span data-ttu-id="e5542-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5542-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5542-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e5542-118">-ServerName</span></span>
<span data-ttu-id="e5542-119">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e5542-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="e5542-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e5542-120">-Confirm</span></span>
<span data-ttu-id="e5542-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5542-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5542-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5542-122">-WhatIf</span></span>
<span data-ttu-id="e5542-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e5542-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5542-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5542-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5542-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5542-125">CommonParameters</span></span>
<span data-ttu-id="e5542-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5542-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5542-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5542-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5542-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="e5542-128">INPUTS</span></span>

### <span data-ttu-id="e5542-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e5542-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="e5542-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e5542-130">System.String</span></span>

## <span data-ttu-id="e5542-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="e5542-131">OUTPUTS</span></span>

### <span data-ttu-id="e5542-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e5542-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="e5542-133">Notas</span><span class="sxs-lookup"><span data-stu-id="e5542-133">NOTES</span></span>

## <span data-ttu-id="e5542-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5542-134">RELATED LINKS</span></span>
