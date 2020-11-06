---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: e782ef221474ab3a041fddc7628157fd999796d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428747"
---
# <span data-ttu-id="d7567-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7567-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="d7567-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7567-102">SYNOPSIS</span></span>
<span data-ttu-id="d7567-103">Obtém informações sobre um administrador do Azure AD para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7567-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7567-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7567-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7567-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7567-105">DESCRIPTION</span></span>
<span data-ttu-id="d7567-106">O cmdlet **Get-AzureRmSqlServerActiveDirectoryAdministrator** Obtém informações sobre um administrador do Azure Active Directory (Azure AD) para um servidor AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d7567-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="d7567-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7567-107">EXAMPLES</span></span>

### <span data-ttu-id="d7567-108">Exemplo 1: Obtém informações sobre o administrador de um servidor</span><span class="sxs-lookup"><span data-stu-id="d7567-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="d7567-109">Esse comando obtém informações sobre um administrador do Azure AD para um servidor chamado Server01 que está associado a um grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d7567-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d7567-110">OS</span><span class="sxs-lookup"><span data-stu-id="d7567-110">PARAMETERS</span></span>

### <span data-ttu-id="d7567-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7567-111">-DefaultProfile</span></span>
<span data-ttu-id="d7567-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d7567-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7567-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7567-114">Especifica o nome do grupo de recursos ao qual o SQL Server está atribuído.</span><span class="sxs-lookup"><span data-stu-id="d7567-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="d7567-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d7567-115">-ServerName</span></span>
<span data-ttu-id="d7567-116">Especifica o nome do SQL Server para o qual este cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="d7567-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="d7567-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7567-117">-Confirm</span></span>
<span data-ttu-id="d7567-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7567-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7567-119">-WhatIf</span></span>
<span data-ttu-id="d7567-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7567-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7567-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7567-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7567-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7567-122">CommonParameters</span></span>
<span data-ttu-id="d7567-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7567-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7567-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7567-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7567-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7567-125">INPUTS</span></span>

### <span data-ttu-id="d7567-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d7567-126">None</span></span>
<span data-ttu-id="d7567-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d7567-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7567-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7567-128">OUTPUTS</span></span>

### <span data-ttu-id="d7567-129">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="d7567-129">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="d7567-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7567-130">NOTES</span></span>

## <span data-ttu-id="d7567-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7567-131">RELATED LINKS</span></span>

[<span data-ttu-id="d7567-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7567-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="d7567-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7567-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="d7567-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d7567-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


