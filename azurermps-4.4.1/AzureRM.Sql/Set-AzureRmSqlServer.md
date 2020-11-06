---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: 9eb0e0503d1a7a7b71cac8f9f71a7c2f18847bca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429023"
---
# <span data-ttu-id="68359-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="68359-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="68359-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68359-102">SYNOPSIS</span></span>
<span data-ttu-id="68359-103">Modifica as propriedades de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="68359-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68359-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68359-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68359-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68359-105">DESCRIPTION</span></span>
<span data-ttu-id="68359-106">O cmdlet **set-AzureRmSqlServer** modifica as propriedades de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="68359-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="68359-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68359-107">EXAMPLES</span></span>

### <span data-ttu-id="68359-108">Exemplo 1: redefinir a senha de administrador</span><span class="sxs-lookup"><span data-stu-id="68359-108">Example 1: Reset the administrator password</span></span>
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
```

<span data-ttu-id="68359-109">Esse comando redefine a senha de administrador no servidor AzureSQL chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="68359-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="68359-110">OS</span><span class="sxs-lookup"><span data-stu-id="68359-110">PARAMETERS</span></span>

### <span data-ttu-id="68359-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="68359-111">-AssignIdentity</span></span>
<span data-ttu-id="68359-112">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="68359-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="68359-113">-Force</span><span class="sxs-lookup"><span data-stu-id="68359-113">-Force</span></span>
<span data-ttu-id="68359-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="68359-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68359-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68359-115">-ResourceGroupName</span></span>
<span data-ttu-id="68359-116">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="68359-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="68359-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="68359-117">-ServerName</span></span>
<span data-ttu-id="68359-118">Especifica o nome do servidor que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="68359-118">Specifies the name of the server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="68359-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="68359-119">-ServerVersion</span></span>
<span data-ttu-id="68359-120">Especifica a versão para a qual esse cmdlet altera o servidor.</span><span class="sxs-lookup"><span data-stu-id="68359-120">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="68359-121">Os valores aceitáveis para esse parâmetro são: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="68359-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="68359-122">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="68359-122">-SqlAdministratorPassword</span></span>
<span data-ttu-id="68359-123">Especifica uma nova senha, como uma **SecureString** , para o administrador do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="68359-123">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="68359-124">Para obter uma **SecureString** , use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="68359-124">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="68359-125">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="68359-125">For more information, type `Get-Help
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

### <span data-ttu-id="68359-126">-Marcas</span><span class="sxs-lookup"><span data-stu-id="68359-126">-Tags</span></span>
<span data-ttu-id="68359-127">Especifica um dicionário de marcas que este cmdlet associa ao servidor.</span><span class="sxs-lookup"><span data-stu-id="68359-127">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="68359-128">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="68359-128">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="68359-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="68359-129">For example:</span></span>

<span data-ttu-id="68359-130">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="68359-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="68359-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68359-131">-Confirm</span></span>
<span data-ttu-id="68359-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68359-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68359-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68359-133">-WhatIf</span></span>
<span data-ttu-id="68359-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68359-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68359-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68359-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68359-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68359-136">-DefaultProfile</span></span>
<span data-ttu-id="68359-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68359-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68359-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68359-138">CommonParameters</span></span>
<span data-ttu-id="68359-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68359-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68359-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68359-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68359-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68359-141">INPUTS</span></span>

## <span data-ttu-id="68359-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68359-142">OUTPUTS</span></span>

### <span data-ttu-id="68359-143">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="68359-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="68359-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68359-144">NOTES</span></span>

## <span data-ttu-id="68359-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68359-145">RELATED LINKS</span></span>

[<span data-ttu-id="68359-146">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="68359-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)