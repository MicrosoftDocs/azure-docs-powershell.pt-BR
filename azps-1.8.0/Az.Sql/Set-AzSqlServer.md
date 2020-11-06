---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: 24249be1d2b5b203a207d72ebd29ec691a90c39a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598765"
---
# <span data-ttu-id="fceae-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="fceae-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="fceae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fceae-102">SYNOPSIS</span></span>
<span data-ttu-id="fceae-103">Modifica as propriedades de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="fceae-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="fceae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fceae-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fceae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fceae-105">DESCRIPTION</span></span>
<span data-ttu-id="fceae-106">O cmdlet **set-AzSqlServer** modifica as propriedades de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fceae-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="fceae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fceae-107">EXAMPLES</span></span>

### <span data-ttu-id="fceae-108">Exemplo 1: redefinir a senha de administrador</span><span class="sxs-lookup"><span data-stu-id="fceae-108">Example 1: Reset the administrator password</span></span>
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

<span data-ttu-id="fceae-109">Esse comando redefine a senha de administrador no servidor AzureSQL chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="fceae-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="fceae-110">OS</span><span class="sxs-lookup"><span data-stu-id="fceae-110">PARAMETERS</span></span>

### <span data-ttu-id="fceae-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fceae-111">-AssignIdentity</span></span>
<span data-ttu-id="fceae-112">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="fceae-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fceae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fceae-113">-DefaultProfile</span></span>
<span data-ttu-id="fceae-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fceae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fceae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fceae-115">-Force</span></span>
<span data-ttu-id="fceae-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fceae-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fceae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fceae-117">-ResourceGroupName</span></span>
<span data-ttu-id="fceae-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fceae-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fceae-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fceae-119">-ServerName</span></span>
<span data-ttu-id="fceae-120">Especifica o nome do servidor que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="fceae-120">Specifies the name of the server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fceae-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="fceae-121">-ServerVersion</span></span>
<span data-ttu-id="fceae-122">Especifica a versão para a qual esse cmdlet altera o servidor.</span><span class="sxs-lookup"><span data-stu-id="fceae-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="fceae-123">Os valores aceitáveis para esse parâmetro são: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="fceae-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="fceae-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="fceae-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="fceae-125">Especifica uma nova senha, como uma **SecureString** , para o administrador do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fceae-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="fceae-126">Para obter uma **SecureString** , use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="fceae-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="fceae-127">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="fceae-127">For more information, type `Get-Help
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

### <span data-ttu-id="fceae-128">-Marcas</span><span class="sxs-lookup"><span data-stu-id="fceae-128">-Tags</span></span>
<span data-ttu-id="fceae-129">Especifica um dicionário de marcas que este cmdlet associa ao servidor.</span><span class="sxs-lookup"><span data-stu-id="fceae-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="fceae-130">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="fceae-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="fceae-131">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fceae-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fceae-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fceae-132">-Confirm</span></span>
<span data-ttu-id="fceae-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fceae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fceae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fceae-134">-WhatIf</span></span>
<span data-ttu-id="fceae-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fceae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fceae-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fceae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fceae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fceae-137">CommonParameters</span></span>
<span data-ttu-id="fceae-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fceae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fceae-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fceae-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fceae-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fceae-140">INPUTS</span></span>

### <span data-ttu-id="fceae-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fceae-141">System.String</span></span>

## <span data-ttu-id="fceae-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fceae-142">OUTPUTS</span></span>

### <span data-ttu-id="fceae-143">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fceae-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="fceae-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fceae-144">NOTES</span></span>

## <span data-ttu-id="fceae-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fceae-145">RELATED LINKS</span></span>

[<span data-ttu-id="fceae-146">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="fceae-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
