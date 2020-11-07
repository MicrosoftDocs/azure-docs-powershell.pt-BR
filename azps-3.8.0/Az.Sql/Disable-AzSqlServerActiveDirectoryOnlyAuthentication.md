---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942017"
---
# <span data-ttu-id="c27c9-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c27c9-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="c27c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c27c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c27c9-103">Desabilita a autenticação do Azure AD para um SQL Server específico.</span><span class="sxs-lookup"><span data-stu-id="c27c9-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="c27c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c27c9-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c27c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c27c9-105">DESCRIPTION</span></span>
<span data-ttu-id="c27c9-106">O cmdlet **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** desabilita o Azure Active Directory (Azure AD) apenas requisito de autenticação para um servidor AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c27c9-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="c27c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c27c9-107">EXAMPLES</span></span>

### <span data-ttu-id="c27c9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c27c9-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="c27c9-109">Esse comando desabilita o Azure Active Directory (Azure AD) apenas os requisitos de autenticação para um servidor AzureSQL chamado Server01 que está associado a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c27c9-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c27c9-110">OS</span><span class="sxs-lookup"><span data-stu-id="c27c9-110">PARAMETERS</span></span>

### <span data-ttu-id="c27c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27c9-111">-DefaultProfile</span></span>
<span data-ttu-id="c27c9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c27c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c27c9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c27c9-113">-ResourceGroupName</span></span>
<span data-ttu-id="c27c9-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c27c9-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c27c9-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c27c9-115">-ServerName</span></span>
<span data-ttu-id="c27c9-116">O nome do Azure SQL Server no qual o administrador do Azure Active Directory está.</span><span class="sxs-lookup"><span data-stu-id="c27c9-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c27c9-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c27c9-117">-Confirm</span></span>
<span data-ttu-id="c27c9-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c27c9-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c27c9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c27c9-119">-WhatIf</span></span>
<span data-ttu-id="c27c9-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c27c9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c27c9-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c27c9-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c27c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27c9-122">CommonParameters</span></span>
<span data-ttu-id="c27c9-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c27c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27c9-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c27c9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27c9-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c27c9-125">INPUTS</span></span>

### <span data-ttu-id="c27c9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c27c9-126">System.String</span></span>

## <span data-ttu-id="c27c9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c27c9-127">OUTPUTS</span></span>

### <span data-ttu-id="c27c9-128">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="c27c9-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="c27c9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c27c9-129">NOTES</span></span>

## <span data-ttu-id="c27c9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c27c9-130">RELATED LINKS</span></span>

[<span data-ttu-id="c27c9-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c27c9-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c27c9-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c27c9-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c27c9-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c27c9-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c27c9-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c27c9-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
