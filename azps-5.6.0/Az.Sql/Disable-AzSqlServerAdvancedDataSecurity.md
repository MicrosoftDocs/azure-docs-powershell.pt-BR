---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 4abe17fb272e97637bbd43a69401f9c101f14ef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887334"
---
# <span data-ttu-id="5d68c-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="5d68c-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="5d68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d68c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d68c-103">Desabilita a Segurança Avançada de Dados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="5d68c-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="5d68c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5d68c-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d68c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5d68c-105">DESCRIPTION</span></span>
<span data-ttu-id="5d68c-106">O cmdlet **Disable-AzSqlServerAdvancedDataSecurity** desabilita a Segurança Avançada de Dados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="5d68c-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="5d68c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d68c-107">EXAMPLES</span></span>

### <span data-ttu-id="5d68c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5d68c-108">Example 1</span></span>
### <span data-ttu-id="5d68c-109">Exemplo 2: Desabilitar a Segurança Avançada de Dados do servidor</span><span class="sxs-lookup"><span data-stu-id="5d68c-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="5d68c-110">Exemplo 3: Desabilitar a Segurança Avançada de Dados do servidor a partir do recurso de servidor</span><span class="sxs-lookup"><span data-stu-id="5d68c-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="5d68c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5d68c-111">PARAMETERS</span></span>

### <span data-ttu-id="5d68c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d68c-112">-DefaultProfile</span></span>
<span data-ttu-id="5d68c-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d68c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d68c-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d68c-114">-InputObject</span></span>
<span data-ttu-id="5d68c-115">O objeto server a ser usado com a operação de política de Segurança de Dados Avançada</span><span class="sxs-lookup"><span data-stu-id="5d68c-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="5d68c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d68c-116">-ResourceGroupName</span></span>
<span data-ttu-id="5d68c-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d68c-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d68c-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d68c-118">-ServerName</span></span>
<span data-ttu-id="5d68c-119">SQL nome do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5d68c-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="5d68c-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d68c-120">-Confirm</span></span>
<span data-ttu-id="5d68c-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d68c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d68c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d68c-122">-WhatIf</span></span>
<span data-ttu-id="5d68c-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d68c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d68c-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d68c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d68c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d68c-125">CommonParameters</span></span>
<span data-ttu-id="5d68c-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d68c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d68c-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d68c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d68c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d68c-128">INPUTS</span></span>

### <span data-ttu-id="5d68c-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5d68c-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="5d68c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5d68c-130">System.String</span></span>

## <span data-ttu-id="5d68c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5d68c-131">OUTPUTS</span></span>

### <span data-ttu-id="5d68c-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5d68c-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="5d68c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="5d68c-133">NOTES</span></span>

## <span data-ttu-id="5d68c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d68c-134">RELATED LINKS</span></span>
