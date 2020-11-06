---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431763"
---
# <span data-ttu-id="542a8-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="542a8-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="542a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="542a8-102">SYNOPSIS</span></span>
<span data-ttu-id="542a8-103">Provisiona um administrador do Azure AD para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="542a8-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="542a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="542a8-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="542a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="542a8-105">DESCRIPTION</span></span>
<span data-ttu-id="542a8-106">O cmdlet **set-AzureRmSqlServerActiveDirectoryAdministrator** provisiona um administrador do Azure Active Directory (Azure AD) para AzureSQL Server na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="542a8-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="542a8-107">Você pode provisionar apenas um administrador de cada vez.</span><span class="sxs-lookup"><span data-stu-id="542a8-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="542a8-108">Os seguintes membros do Azure AD podem ser provisionados como um administrador do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="542a8-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="542a8-109">Membros nativos do Azure AD</span><span class="sxs-lookup"><span data-stu-id="542a8-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="542a8-110">Membros federados do Azure AD</span><span class="sxs-lookup"><span data-stu-id="542a8-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="542a8-111">Membros importados de outros anúncios do Azure que são membros nativos ou federados</span><span class="sxs-lookup"><span data-stu-id="542a8-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="542a8-112">Grupos do Azure AD criados como grupos de segurança</span><span class="sxs-lookup"><span data-stu-id="542a8-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="542a8-113">Contas da Microsoft, como os dos domínios Outlook.com, Hotmail.com ou Live.com, não são compatíveis com administradores.</span><span class="sxs-lookup"><span data-stu-id="542a8-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="542a8-114">Não há suporte para outras contas de convidado, como aquelas dos domínios Gmail.com ou Yahoo.com como administradores.</span><span class="sxs-lookup"><span data-stu-id="542a8-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="542a8-115">Recomendamos que você provisione um grupo dedicado do Azure AD como administrador.</span><span class="sxs-lookup"><span data-stu-id="542a8-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="542a8-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="542a8-116">EXAMPLES</span></span>

### <span data-ttu-id="542a8-117">Exemplo 1: configurar um grupo de administradores para um servidor</span><span class="sxs-lookup"><span data-stu-id="542a8-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="542a8-118">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="542a8-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="542a8-119">Este servidor está associado à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="542a8-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="542a8-120">Exemplo 2: prover um usuário administrador para um servidor</span><span class="sxs-lookup"><span data-stu-id="542a8-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="542a8-121">Esse comando provisiona um usuário do Azure AD como administrador para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="542a8-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="542a8-122">Exemplo 3: provisionar um grupo de administradores especificando sua ID</span><span class="sxs-lookup"><span data-stu-id="542a8-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="542a8-123">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="542a8-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="542a8-124">O comando especifica uma ID para o parâmetro *ObjectID* .</span><span class="sxs-lookup"><span data-stu-id="542a8-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="542a8-125">Isso garante que o comando tenha êxito mesmo se o nome de exibição do grupo não for exclusivo.</span><span class="sxs-lookup"><span data-stu-id="542a8-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="542a8-126">OS</span><span class="sxs-lookup"><span data-stu-id="542a8-126">PARAMETERS</span></span>

### <span data-ttu-id="542a8-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="542a8-127">-DisplayName</span></span>
<span data-ttu-id="542a8-128">Especifica o nome de exibição do administrador do Azure AD que este cmdlet provisiona.</span><span class="sxs-lookup"><span data-stu-id="542a8-128">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="542a8-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="542a8-129">-ObjectId</span></span>
<span data-ttu-id="542a8-130">Especifica a ID exclusiva do administrador do Azure AD que este cmdlet provisiona.</span><span class="sxs-lookup"><span data-stu-id="542a8-130">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="542a8-131">Se o nome para exibição não for exclusivo, você deve especificar um valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="542a8-131">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="542a8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="542a8-132">-ResourceGroupName</span></span>
<span data-ttu-id="542a8-133">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="542a8-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="542a8-134">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="542a8-134">-ServerName</span></span>
<span data-ttu-id="542a8-135">Especifica o nome do SQL Server para o qual esse cmdlet provisiona um administrador.</span><span class="sxs-lookup"><span data-stu-id="542a8-135">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="542a8-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="542a8-136">-Confirm</span></span>
<span data-ttu-id="542a8-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="542a8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="542a8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="542a8-138">-WhatIf</span></span>
<span data-ttu-id="542a8-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="542a8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="542a8-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="542a8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="542a8-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542a8-141">-DefaultProfile</span></span>
<span data-ttu-id="542a8-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="542a8-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="542a8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542a8-143">CommonParameters</span></span>
<span data-ttu-id="542a8-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542a8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542a8-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542a8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542a8-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="542a8-146">INPUTS</span></span>

## <span data-ttu-id="542a8-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="542a8-147">OUTPUTS</span></span>

### <span data-ttu-id="542a8-148">Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="542a8-148">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="542a8-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="542a8-149">NOTES</span></span>

## <span data-ttu-id="542a8-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="542a8-150">RELATED LINKS</span></span>

[<span data-ttu-id="542a8-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="542a8-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="542a8-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="542a8-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="542a8-153">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="542a8-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


