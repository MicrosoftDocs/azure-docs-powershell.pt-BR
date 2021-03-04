---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 09b7ebf1f88479bca847566b2da93feb83b18571
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888163"
---
# <span data-ttu-id="915a3-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="915a3-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="915a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="915a3-102">SYNOPSIS</span></span>
<span data-ttu-id="915a3-103">Obtém informações sobre um administrador do Azure AD para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="915a3-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="915a3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="915a3-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="915a3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="915a3-105">DESCRIPTION</span></span>
<span data-ttu-id="915a3-106">O cmdlet **Get-AzSqlServerActiveDirectoryAdministrator** obtém informações sobre um administrador do Azure Active Directory (Azure AD) para um Servidor do AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="915a3-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="915a3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="915a3-107">EXAMPLES</span></span>

### <span data-ttu-id="915a3-108">Exemplo 1: obtém informações sobre um administrador para um servidor</span><span class="sxs-lookup"><span data-stu-id="915a3-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="915a3-109">Este comando obtém informações sobre um administrador do Azure AD para um servidor chamado Server01 associado a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="915a3-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="915a3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="915a3-110">PARAMETERS</span></span>

### <span data-ttu-id="915a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="915a3-111">-DefaultProfile</span></span>
<span data-ttu-id="915a3-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="915a3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="915a3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="915a3-113">-ResourceGroupName</span></span>
<span data-ttu-id="915a3-114">Especifica o nome do grupo de recursos ao qual o SQL Server é atribuído.</span><span class="sxs-lookup"><span data-stu-id="915a3-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="915a3-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="915a3-115">-ServerName</span></span>
<span data-ttu-id="915a3-116">Especifica o nome do SQL Server para o qual este cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="915a3-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915a3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="915a3-117">-Confirm</span></span>
<span data-ttu-id="915a3-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="915a3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="915a3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="915a3-119">-WhatIf</span></span>
<span data-ttu-id="915a3-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="915a3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="915a3-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="915a3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="915a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915a3-122">CommonParameters</span></span>
<span data-ttu-id="915a3-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="915a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915a3-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="915a3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915a3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="915a3-125">INPUTS</span></span>

### <span data-ttu-id="915a3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="915a3-126">System.String</span></span>

## <span data-ttu-id="915a3-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="915a3-127">OUTPUTS</span></span>

### <span data-ttu-id="915a3-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="915a3-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="915a3-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="915a3-129">NOTES</span></span>

## <span data-ttu-id="915a3-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="915a3-130">RELATED LINKS</span></span>

[<span data-ttu-id="915a3-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="915a3-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="915a3-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="915a3-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="915a3-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="915a3-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="915a3-134">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="915a3-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


