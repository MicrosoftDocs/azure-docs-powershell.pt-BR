---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777384"
---
# <span data-ttu-id="41e1d-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="41e1d-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="41e1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="41e1d-103">Modifica as propriedades de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="41e1d-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="41e1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41e1d-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41e1d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41e1d-105">DESCRIPTION</span></span>
<span data-ttu-id="41e1d-106">O cmdlet **set-AzSqlServer** modifica as propriedades de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="41e1d-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="41e1d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41e1d-107">EXAMPLES</span></span>

### <span data-ttu-id="41e1d-108">Exemplo 1: redefinir a senha de administrador</span><span class="sxs-lookup"><span data-stu-id="41e1d-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="41e1d-109">Esse comando redefine a senha de administrador no servidor AzureSQL chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="41e1d-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="41e1d-110">OS</span><span class="sxs-lookup"><span data-stu-id="41e1d-110">PARAMETERS</span></span>

### <span data-ttu-id="41e1d-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="41e1d-111">-AssignIdentity</span></span>
<span data-ttu-id="41e1d-112">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="41e1d-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="41e1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e1d-113">-DefaultProfile</span></span>
<span data-ttu-id="41e1d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="41e1d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41e1d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="41e1d-115">-Force</span></span>
<span data-ttu-id="41e1d-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="41e1d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41e1d-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="41e1d-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="41e1d-118">Usa um sinalizador, habilitado/desabilitado, para especificar se o acesso à rede pública ao servidor é permitido ou não.</span><span class="sxs-lookup"><span data-stu-id="41e1d-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="41e1d-119">Quando desabilitado, somente as conexões feitas por meio de links privados podem chegar a esse servidor.</span><span class="sxs-lookup"><span data-stu-id="41e1d-119">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e1d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e1d-120">-ResourceGroupName</span></span>
<span data-ttu-id="41e1d-121">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="41e1d-121">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="41e1d-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="41e1d-122">-ServerName</span></span>
<span data-ttu-id="41e1d-123">Especifica o nome do servidor que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="41e1d-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41e1d-124">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="41e1d-124">-ServerVersion</span></span>
<span data-ttu-id="41e1d-125">Especifica a versão para a qual esse cmdlet altera o servidor.</span><span class="sxs-lookup"><span data-stu-id="41e1d-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="41e1d-126">Os valores aceitáveis para esse parâmetro são: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="41e1d-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="41e1d-127">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="41e1d-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="41e1d-128">Especifica uma nova senha, como uma **SecureString** , para o administrador do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="41e1d-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="41e1d-129">Para obter uma **SecureString** , use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="41e1d-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="41e1d-130">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="41e1d-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e1d-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="41e1d-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="41e1d-132">A versão do TLS mínima a ser aplicada ao SQL Server</span><span class="sxs-lookup"><span data-stu-id="41e1d-132">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="41e1d-133">-Marcas</span><span class="sxs-lookup"><span data-stu-id="41e1d-133">-Tags</span></span>
<span data-ttu-id="41e1d-134">Especifica um dicionário de marcas que este cmdlet associa ao servidor.</span><span class="sxs-lookup"><span data-stu-id="41e1d-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="41e1d-135">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="41e1d-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="41e1d-136">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="41e1d-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="41e1d-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41e1d-137">-Confirm</span></span>
<span data-ttu-id="41e1d-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41e1d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41e1d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41e1d-139">-WhatIf</span></span>
<span data-ttu-id="41e1d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41e1d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41e1d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41e1d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41e1d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e1d-142">CommonParameters</span></span>
<span data-ttu-id="41e1d-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e1d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e1d-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41e1d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e1d-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41e1d-145">INPUTS</span></span>

### <span data-ttu-id="41e1d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="41e1d-146">System.String</span></span>

## <span data-ttu-id="41e1d-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41e1d-147">OUTPUTS</span></span>

### <span data-ttu-id="41e1d-148">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="41e1d-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="41e1d-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41e1d-149">NOTES</span></span>

## <span data-ttu-id="41e1d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41e1d-150">RELATED LINKS</span></span>

[<span data-ttu-id="41e1d-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="41e1d-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
