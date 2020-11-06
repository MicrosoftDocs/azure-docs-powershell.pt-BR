---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: b29af2f5f8931876d1bf23d05072e92dc4eb588e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599016"
---
# <span data-ttu-id="23a2f-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="23a2f-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="23a2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="23a2f-103">Obtém a política de conexão segura para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23a2f-103">Gets the secure connection policy for a database.</span></span>

## <span data-ttu-id="23a2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23a2f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23a2f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="23a2f-106">O cmdlet **Get-AzSqlDatabaseSecureConnectionPolicy** Obtém a política de canal criptografado de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="23a2f-106">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="23a2f-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23a2f-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="23a2f-108">Depois que o cmdlet é executado com êxito, ele retorna um objeto que descreve a política de canal criptografado atual e também os identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23a2f-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="23a2f-109">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="23a2f-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="23a2f-110">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="23a2f-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="23a2f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23a2f-111">EXAMPLES</span></span>

### <span data-ttu-id="23a2f-112">Exemplo 1: obter a política de canal criptografado de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="23a2f-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
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

<span data-ttu-id="23a2f-113">Esse comando obtém a política de canal criptografado de um banco de dados SQL do Azure chamado database01 localizado no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="23a2f-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="23a2f-114">OS</span><span class="sxs-lookup"><span data-stu-id="23a2f-114">PARAMETERS</span></span>

### <span data-ttu-id="23a2f-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23a2f-115">-DatabaseName</span></span>
<span data-ttu-id="23a2f-116">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23a2f-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="23a2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a2f-117">-DefaultProfile</span></span>
<span data-ttu-id="23a2f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="23a2f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23a2f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23a2f-119">-ResourceGroupName</span></span>
<span data-ttu-id="23a2f-120">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="23a2f-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="23a2f-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="23a2f-121">-ServerName</span></span>
<span data-ttu-id="23a2f-122">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23a2f-122">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="23a2f-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23a2f-123">-Confirm</span></span>
<span data-ttu-id="23a2f-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23a2f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23a2f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23a2f-125">-WhatIf</span></span>
<span data-ttu-id="23a2f-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23a2f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23a2f-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23a2f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23a2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a2f-128">CommonParameters</span></span>
<span data-ttu-id="23a2f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a2f-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23a2f-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a2f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23a2f-131">INPUTS</span></span>

### <span data-ttu-id="23a2f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="23a2f-132">System.String</span></span>

## <span data-ttu-id="23a2f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23a2f-133">OUTPUTS</span></span>

### <span data-ttu-id="23a2f-134">Microsoft. Azure. Commands. Sql. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="23a2f-134">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="23a2f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23a2f-135">NOTES</span></span>

## <span data-ttu-id="23a2f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23a2f-136">RELATED LINKS</span></span>
