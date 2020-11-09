---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281702"
---
# <span data-ttu-id="a9612-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a9612-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a9612-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9612-102">SYNOPSIS</span></span>
<span data-ttu-id="a9612-103">Provisiona um administrador do Azure AD para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a9612-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="a9612-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9612-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9612-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9612-105">DESCRIPTION</span></span>
<span data-ttu-id="a9612-106">O cmdlet **set-AzSqlServerActiveDirectoryAdministrator** provisiona um administrador do Azure Active Directory (Azure AD) para AzureSQL Server na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a9612-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="a9612-107">Você pode provisionar apenas um administrador de cada vez.</span><span class="sxs-lookup"><span data-stu-id="a9612-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="a9612-108">Os seguintes membros do Azure AD podem ser provisionados como um administrador do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="a9612-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="a9612-109">Membros nativos do Azure AD</span><span class="sxs-lookup"><span data-stu-id="a9612-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="a9612-110">Membros federados do Azure AD</span><span class="sxs-lookup"><span data-stu-id="a9612-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="a9612-111">Membros importados de outros anúncios do Azure que são membros nativos ou federados</span><span class="sxs-lookup"><span data-stu-id="a9612-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="a9612-112">Grupos do Azure AD criados como grupos de segurança contas da Microsoft, como os dos domínios Outlook.com, Hotmail.com ou Live.com, não têm suporte como administradores.</span><span class="sxs-lookup"><span data-stu-id="a9612-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a9612-113">Não há suporte para outras contas de convidado, como aquelas dos domínios Gmail.com ou Yahoo.com como administradores.</span><span class="sxs-lookup"><span data-stu-id="a9612-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a9612-114">Recomendamos que você provisione um grupo dedicado do Azure AD como administrador.</span><span class="sxs-lookup"><span data-stu-id="a9612-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="a9612-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9612-115">EXAMPLES</span></span>

### <span data-ttu-id="a9612-116">Exemplo 1: configurar um grupo de administradores para um servidor</span><span class="sxs-lookup"><span data-stu-id="a9612-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="a9612-117">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="a9612-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="a9612-118">Este servidor está associado à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9612-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a9612-119">Exemplo 2: prover um usuário administrador para um servidor</span><span class="sxs-lookup"><span data-stu-id="a9612-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="a9612-120">Esse comando provisiona um usuário do Azure AD como administrador para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="a9612-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="a9612-121">Exemplo 3: provisionar um grupo de administradores especificando sua ID</span><span class="sxs-lookup"><span data-stu-id="a9612-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="a9612-122">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="a9612-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="a9612-123">O comando especifica uma ID para o parâmetro *ObjectID* .</span><span class="sxs-lookup"><span data-stu-id="a9612-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="a9612-124">Isso garante que o comando tenha êxito mesmo se o nome de exibição do grupo não for exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a9612-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="a9612-125">OS</span><span class="sxs-lookup"><span data-stu-id="a9612-125">PARAMETERS</span></span>

### <span data-ttu-id="a9612-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9612-126">-DefaultProfile</span></span>
<span data-ttu-id="a9612-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9612-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9612-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9612-128">-DisplayName</span></span>
<span data-ttu-id="a9612-129">Especifica o nome de exibição do administrador do Azure AD que este cmdlet provisiona.</span><span class="sxs-lookup"><span data-stu-id="a9612-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="a9612-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a9612-130">-ObjectId</span></span>
<span data-ttu-id="a9612-131">Especifica a ID exclusiva do administrador do Azure AD que este cmdlet provisiona.</span><span class="sxs-lookup"><span data-stu-id="a9612-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="a9612-132">Se o nome para exibição não for exclusivo, você deve especificar um valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a9612-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9612-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9612-133">-ResourceGroupName</span></span>
<span data-ttu-id="a9612-134">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a9612-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a9612-135">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a9612-135">-ServerName</span></span>
<span data-ttu-id="a9612-136">Especifica o nome do SQL Server para o qual esse cmdlet provisiona um administrador.</span><span class="sxs-lookup"><span data-stu-id="a9612-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="a9612-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9612-137">-Confirm</span></span>
<span data-ttu-id="a9612-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9612-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9612-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9612-139">-WhatIf</span></span>
<span data-ttu-id="a9612-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9612-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9612-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9612-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9612-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9612-142">CommonParameters</span></span>
<span data-ttu-id="a9612-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9612-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9612-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9612-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9612-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9612-145">INPUTS</span></span>

### <span data-ttu-id="a9612-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a9612-146">System.String</span></span>

### <span data-ttu-id="a9612-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a9612-147">System.Guid</span></span>

## <span data-ttu-id="a9612-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9612-148">OUTPUTS</span></span>

### <span data-ttu-id="a9612-149">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a9612-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a9612-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9612-150">NOTES</span></span>

## <span data-ttu-id="a9612-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9612-151">RELATED LINKS</span></span>

[<span data-ttu-id="a9612-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a9612-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a9612-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a9612-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a9612-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a9612-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="a9612-155">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a9612-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


