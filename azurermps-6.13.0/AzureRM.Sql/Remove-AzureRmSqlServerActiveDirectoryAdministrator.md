---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: c8b186c55161732a014e281162fa5d6131e72115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440007"
---
# <span data-ttu-id="6e082-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6e082-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="6e082-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e082-102">SYNOPSIS</span></span>
<span data-ttu-id="6e082-103">Remove um administrador do Azure AD para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e082-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e082-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e082-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e082-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e082-105">DESCRIPTION</span></span>
<span data-ttu-id="6e082-106">O cmdlet **Remove-AzureRmSqlServerActiveDirectoryAdministrator** remove um administrador do Azure Active Directory (Azure AD) para AzureSQL Server na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6e082-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="6e082-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e082-107">EXAMPLES</span></span>

### <span data-ttu-id="6e082-108">Exemplo 1: remover um administrador</span><span class="sxs-lookup"><span data-stu-id="6e082-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="6e082-109">Esse comando Remove o administrador do Azure AD do servidor chamado Server01 associado à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e082-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="6e082-110">OS</span><span class="sxs-lookup"><span data-stu-id="6e082-110">PARAMETERS</span></span>

### <span data-ttu-id="6e082-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e082-111">-DefaultProfile</span></span>
<span data-ttu-id="6e082-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6e082-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e082-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6e082-113">-Force</span></span>
<span data-ttu-id="6e082-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6e082-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e082-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e082-115">-ResourceGroupName</span></span>
<span data-ttu-id="6e082-116">Especifica o nome do grupo de recursos ao qual o SQL Server está atribuído.</span><span class="sxs-lookup"><span data-stu-id="6e082-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="6e082-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6e082-117">-ServerName</span></span>
<span data-ttu-id="6e082-118">Especifica o nome do SQL Server para o qual esse cmdlet Remove um administrador.</span><span class="sxs-lookup"><span data-stu-id="6e082-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="6e082-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e082-119">-Confirm</span></span>
<span data-ttu-id="6e082-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e082-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e082-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e082-121">-WhatIf</span></span>
<span data-ttu-id="6e082-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e082-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e082-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e082-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e082-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e082-124">CommonParameters</span></span>
<span data-ttu-id="6e082-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e082-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e082-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e082-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e082-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e082-127">INPUTS</span></span>

### <span data-ttu-id="6e082-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6e082-128">System.String</span></span>

## <span data-ttu-id="6e082-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e082-129">OUTPUTS</span></span>

### <span data-ttu-id="6e082-130">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="6e082-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="6e082-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e082-131">NOTES</span></span>

## <span data-ttu-id="6e082-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e082-132">RELATED LINKS</span></span>

[<span data-ttu-id="6e082-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6e082-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="6e082-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6e082-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="6e082-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="6e082-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


