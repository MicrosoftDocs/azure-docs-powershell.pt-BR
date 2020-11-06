---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: f7d6dab2629dc8247cb404d1de2dc58b21fc8a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433361"
---
# <span data-ttu-id="800f1-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="800f1-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="800f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="800f1-102">SYNOPSIS</span></span>
<span data-ttu-id="800f1-103">Modifica as propriedades de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="800f1-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="800f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="800f1-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="800f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="800f1-105">DESCRIPTION</span></span>
<span data-ttu-id="800f1-106">O cmdlet **set-AzureRmSqlServer** modifica as propriedades de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="800f1-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="800f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="800f1-107">EXAMPLES</span></span>

### <span data-ttu-id="800f1-108">Exemplo 1: redefinir a senha de administrador</span><span class="sxs-lookup"><span data-stu-id="800f1-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
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

<span data-ttu-id="800f1-109">Esse comando redefine a senha de administrador no servidor AzureSQL chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="800f1-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="800f1-110">OS</span><span class="sxs-lookup"><span data-stu-id="800f1-110">PARAMETERS</span></span>

### <span data-ttu-id="800f1-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="800f1-111">-AssignIdentity</span></span>
<span data-ttu-id="800f1-112">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="800f1-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800f1-113">-DefaultProfile</span></span>
<span data-ttu-id="800f1-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="800f1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="800f1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="800f1-115">-Force</span></span>
<span data-ttu-id="800f1-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="800f1-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="800f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="800f1-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="800f1-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="800f1-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="800f1-119">-ServerName</span></span>
<span data-ttu-id="800f1-120">Especifica o nome do servidor que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="800f1-120">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800f1-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="800f1-121">-ServerVersion</span></span>
<span data-ttu-id="800f1-122">Especifica a versão para a qual esse cmdlet altera o servidor.</span><span class="sxs-lookup"><span data-stu-id="800f1-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="800f1-123">Os valores aceitáveis para esse parâmetro são: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="800f1-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="800f1-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="800f1-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="800f1-125">Especifica uma nova senha, como uma **SecureString** , para o administrador do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="800f1-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="800f1-126">Para obter uma **SecureString** , use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="800f1-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="800f1-127">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="800f1-127">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800f1-128">-Marcas</span><span class="sxs-lookup"><span data-stu-id="800f1-128">-Tags</span></span>
<span data-ttu-id="800f1-129">Especifica um dicionário de marcas que este cmdlet associa ao servidor.</span><span class="sxs-lookup"><span data-stu-id="800f1-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="800f1-130">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="800f1-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="800f1-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="800f1-131">For example:</span></span>

<span data-ttu-id="800f1-132">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="800f1-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800f1-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="800f1-133">-Confirm</span></span>
<span data-ttu-id="800f1-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="800f1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="800f1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800f1-135">-WhatIf</span></span>
<span data-ttu-id="800f1-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="800f1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="800f1-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="800f1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="800f1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800f1-138">CommonParameters</span></span>
<span data-ttu-id="800f1-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="800f1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800f1-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800f1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800f1-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="800f1-141">INPUTS</span></span>

### <span data-ttu-id="800f1-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="800f1-142">None</span></span>
<span data-ttu-id="800f1-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="800f1-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="800f1-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="800f1-144">OUTPUTS</span></span>

### <span data-ttu-id="800f1-145">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="800f1-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="800f1-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="800f1-146">NOTES</span></span>

## <span data-ttu-id="800f1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="800f1-147">RELATED LINKS</span></span>

[<span data-ttu-id="800f1-148">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="800f1-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
