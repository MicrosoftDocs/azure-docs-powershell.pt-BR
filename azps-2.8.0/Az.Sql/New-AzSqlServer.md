---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 0d5eb08c938fe17e4270cd66038a738341937cb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773566"
---
# <span data-ttu-id="a95dd-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a95dd-101">New-AzSqlServer</span></span>

## <span data-ttu-id="a95dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a95dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a95dd-103">Cria um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="a95dd-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="a95dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a95dd-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a95dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a95dd-105">DESCRIPTION</span></span>
<span data-ttu-id="a95dd-106">O cmdlet **New-AzSqlServer** cria um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a95dd-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="a95dd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a95dd-107">EXAMPLES</span></span>

### <span data-ttu-id="a95dd-108">Exemplo 1: criar um novo servidor de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="a95dd-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="a95dd-109">Esse comando cria uma versão 12 do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a95dd-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="a95dd-110">OS</span><span class="sxs-lookup"><span data-stu-id="a95dd-110">PARAMETERS</span></span>

### <span data-ttu-id="a95dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a95dd-111">-AsJob</span></span>
<span data-ttu-id="a95dd-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a95dd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a95dd-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a95dd-113">-AssignIdentity</span></span>
<span data-ttu-id="a95dd-114">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="a95dd-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a95dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95dd-115">-DefaultProfile</span></span>
<span data-ttu-id="a95dd-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a95dd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a95dd-117">-Local</span><span class="sxs-lookup"><span data-stu-id="a95dd-117">-Location</span></span>
<span data-ttu-id="a95dd-118">Especifica o local do centro de dados onde esse cmdlet cria o servidor.</span><span class="sxs-lookup"><span data-stu-id="a95dd-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="a95dd-120">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o servidor.</span><span class="sxs-lookup"><span data-stu-id="a95dd-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="a95dd-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a95dd-121">-ServerName</span></span>
<span data-ttu-id="a95dd-122">Especifica o nome do novo servidor.</span><span class="sxs-lookup"><span data-stu-id="a95dd-122">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95dd-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="a95dd-123">-ServerVersion</span></span>
<span data-ttu-id="a95dd-124">Especifica a versão do novo servidor.</span><span class="sxs-lookup"><span data-stu-id="a95dd-124">Specifies the version of the new server.</span></span> <span data-ttu-id="a95dd-125">Os valores aceitáveis para esse parâmetro são: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="a95dd-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="a95dd-126">Especifique 2,0 para criar um servidor da versão 11 ou 12,0 para criar um servidor da versão 12.</span><span class="sxs-lookup"><span data-stu-id="a95dd-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95dd-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="a95dd-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="a95dd-128">Especifica as credenciais de administrador do servidor de banco de dados SQL para o novo servidor.</span><span class="sxs-lookup"><span data-stu-id="a95dd-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="a95dd-129">Para obter um objeto **PSCredential** , use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="a95dd-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="a95dd-130">Para obter mais informações, digite `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a95dd-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95dd-131">-Marcas</span><span class="sxs-lookup"><span data-stu-id="a95dd-131">-Tags</span></span>
<span data-ttu-id="a95dd-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a95dd-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a95dd-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a95dd-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95dd-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a95dd-134">-Confirm</span></span>
<span data-ttu-id="a95dd-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a95dd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a95dd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95dd-136">-WhatIf</span></span>
<span data-ttu-id="a95dd-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a95dd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a95dd-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a95dd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a95dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95dd-139">CommonParameters</span></span>
<span data-ttu-id="a95dd-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95dd-141">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a95dd-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95dd-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a95dd-142">INPUTS</span></span>

### <span data-ttu-id="a95dd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a95dd-143">System.String</span></span>

## <span data-ttu-id="a95dd-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a95dd-144">OUTPUTS</span></span>

### <span data-ttu-id="a95dd-145">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a95dd-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a95dd-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a95dd-146">NOTES</span></span>

## <span data-ttu-id="a95dd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a95dd-147">RELATED LINKS</span></span>

[<span data-ttu-id="a95dd-148">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a95dd-148">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="a95dd-149">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a95dd-149">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="a95dd-150">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a95dd-150">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="a95dd-151">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a95dd-151">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="a95dd-152">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a95dd-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
