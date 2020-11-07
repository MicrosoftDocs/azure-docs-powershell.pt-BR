---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: d160e6cf954240495a9f9b3969d87dab6d880e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773657"
---
# <span data-ttu-id="c6b75-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c6b75-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="c6b75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6b75-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b75-103">Obtém a política de conexão segura para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c6b75-103">Gets the secure connection policy for a database.</span></span> <span data-ttu-id="c6b75-104">A conexão segura será substituída e esse comando será removido em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="c6b75-104">Secure connection is deprecated and this command will be removed in a future release.</span></span> <span data-ttu-id="c6b75-105">Use a lâmina do banco de dados SQL no portal do Azure para exibir as cadeias de conexão</span><span class="sxs-lookup"><span data-stu-id="c6b75-105">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

## <span data-ttu-id="c6b75-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6b75-106">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6b75-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6b75-107">DESCRIPTION</span></span>
<span data-ttu-id="c6b75-108">O cmdlet **Get-AzSqlDatabaseSecureConnectionPolicy** Obtém a política de canal criptografado de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b75-108">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="c6b75-109">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c6b75-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c6b75-110">Depois que o cmdlet é executado com êxito, ele retorna um objeto que descreve a política de canal criptografado atual e também os identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c6b75-110">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="c6b75-111">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="c6b75-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="c6b75-112">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b75-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c6b75-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6b75-113">EXAMPLES</span></span>

### <span data-ttu-id="c6b75-114">Exemplo 1: obter a política de canal criptografado de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="c6b75-114">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="c6b75-115">Esse comando obtém a política de canal criptografado de um banco de dados SQL do Azure chamado database01 localizado no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="c6b75-115">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="c6b75-116">OS</span><span class="sxs-lookup"><span data-stu-id="c6b75-116">PARAMETERS</span></span>

### <span data-ttu-id="c6b75-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6b75-117">-DatabaseName</span></span>
<span data-ttu-id="c6b75-118">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c6b75-118">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6b75-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b75-119">-DefaultProfile</span></span>
<span data-ttu-id="c6b75-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c6b75-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6b75-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b75-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6b75-122">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c6b75-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c6b75-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c6b75-123">-ServerName</span></span>
<span data-ttu-id="c6b75-124">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c6b75-124">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="c6b75-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c6b75-125">-Confirm</span></span>
<span data-ttu-id="c6b75-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6b75-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b75-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b75-127">-WhatIf</span></span>
<span data-ttu-id="c6b75-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6b75-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6b75-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6b75-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b75-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b75-130">CommonParameters</span></span>
<span data-ttu-id="c6b75-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6b75-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b75-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6b75-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b75-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6b75-133">INPUTS</span></span>

### <span data-ttu-id="c6b75-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c6b75-134">System.String</span></span>

## <span data-ttu-id="c6b75-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6b75-135">OUTPUTS</span></span>

### <span data-ttu-id="c6b75-136">Microsoft. Azure. Commands. Sql. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c6b75-136">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="c6b75-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6b75-137">NOTES</span></span>

## <span data-ttu-id="c6b75-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6b75-138">RELATED LINKS</span></span>
