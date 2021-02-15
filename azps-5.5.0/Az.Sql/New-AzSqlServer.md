---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113728"
---
# <span data-ttu-id="1fcd4-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1fcd4-101">New-AzSqlServer</span></span>

## <span data-ttu-id="1fcd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fcd4-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcd4-103">Cria um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="1fcd4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fcd4-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fcd4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1fcd4-105">DESCRIPTION</span></span>
<span data-ttu-id="1fcd4-106">O **cmdlet New-AzSqlServer** cria um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="1fcd4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1fcd4-107">EXAMPLES</span></span>

### <span data-ttu-id="1fcd4-108">Exemplo 1: Criar um novo servidor de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1fcd4-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="1fcd4-109">Esse comando cria um servidor de banco de dados SQL da versão 12 do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="1fcd4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fcd4-110">PARAMETERS</span></span>

### <span data-ttu-id="1fcd4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fcd4-111">-AsJob</span></span>
<span data-ttu-id="1fcd4-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1fcd4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fcd4-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1fcd4-113">-AssignIdentity</span></span>
<span data-ttu-id="1fcd4-114">Gere e atribua uma Identidade do Azure Active Directory para esse servidor para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1fcd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcd4-115">-DefaultProfile</span></span>
<span data-ttu-id="1fcd4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1fcd4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fcd4-117">-Local</span><span class="sxs-lookup"><span data-stu-id="1fcd4-117">-Location</span></span>
<span data-ttu-id="1fcd4-118">Especifica o local do data center onde este cmdlet cria o servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="1fcd4-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1fcd4-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="1fcd4-120">A versão TLS mínima a ser impor para o Sql Server</span><span class="sxs-lookup"><span data-stu-id="1fcd4-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcd4-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="1fcd4-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="1fcd4-122">Leva um sinalizador, habilitado/desabilitado, para especificar se o acesso de rede pública ao servidor é permitido ou não.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="1fcd4-123">Quando desabilitadas, somente as conexões feitas por meio de Links Particulares podem chegar a esse servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="1fcd4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcd4-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fcd4-125">Especifica o nome do grupo de recursos ao qual este cmdlet atribui o servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="1fcd4-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fcd4-126">-ServerName</span></span>
<span data-ttu-id="1fcd4-127">Especifica o nome do novo servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-127">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="1fcd4-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="1fcd4-128">-ServerVersion</span></span>
<span data-ttu-id="1fcd4-129">Especifica a versão do novo servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-129">Specifies the version of the new server.</span></span> <span data-ttu-id="1fcd4-130">Os valores aceitáveis para este parâmetro são: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="1fcd4-131">Especifique 2.0 para criar um servidor de versão 11 ou 12.0 para criar um servidor de versão 12.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="1fcd4-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="1fcd4-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="1fcd4-133">Especifica as credenciais de administrador do servidor de banco de dados SQL para o novo servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="1fcd4-134">Para obter um **objeto PSCredential,** use Get-Credential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="1fcd4-135">Para obter mais informações, digite `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1fcd4-135">For more information, type `Get-Help
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

### <span data-ttu-id="1fcd4-136">-Marcas</span><span class="sxs-lookup"><span data-stu-id="1fcd4-136">-Tags</span></span>
<span data-ttu-id="1fcd4-137">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1fcd4-138">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1fcd4-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1fcd4-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1fcd4-139">-Confirm</span></span>
<span data-ttu-id="1fcd4-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcd4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcd4-141">-WhatIf</span></span>
<span data-ttu-id="1fcd4-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fcd4-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcd4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcd4-144">CommonParameters</span></span>
<span data-ttu-id="1fcd4-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fcd4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcd4-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fcd4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcd4-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="1fcd4-147">INPUTS</span></span>

### <span data-ttu-id="1fcd4-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1fcd4-148">System.String</span></span>

## <span data-ttu-id="1fcd4-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="1fcd4-149">OUTPUTS</span></span>

### <span data-ttu-id="1fcd4-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1fcd4-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1fcd4-151">Notas</span><span class="sxs-lookup"><span data-stu-id="1fcd4-151">NOTES</span></span>

## <span data-ttu-id="1fcd4-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fcd4-152">RELATED LINKS</span></span>

[<span data-ttu-id="1fcd4-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1fcd4-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="1fcd4-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1fcd4-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="1fcd4-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1fcd4-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="1fcd4-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1fcd4-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="1fcd4-157">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="1fcd4-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
