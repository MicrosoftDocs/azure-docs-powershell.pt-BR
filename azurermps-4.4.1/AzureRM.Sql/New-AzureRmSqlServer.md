---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: a754ff33cba0bcf6324be0eb947b592b8fd4a622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603094"
---
# <span data-ttu-id="b0cfd-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b0cfd-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="b0cfd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="b0cfd-103">Cria um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0cfd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0cfd-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0cfd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0cfd-105">DESCRIPTION</span></span>
<span data-ttu-id="b0cfd-106">O cmdlet **New-AzureRmSqlServer** cria um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="b0cfd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0cfd-107">EXAMPLES</span></span>

### <span data-ttu-id="b0cfd-108">Exemplo 1: criar um novo servidor de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="b0cfd-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="b0cfd-109">Esse comando cria uma versão 12 do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="b0cfd-110">OS</span><span class="sxs-lookup"><span data-stu-id="b0cfd-110">PARAMETERS</span></span>

### <span data-ttu-id="b0cfd-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b0cfd-111">-AssignIdentity</span></span>
<span data-ttu-id="b0cfd-112">Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="b0cfd-113">-Local</span><span class="sxs-lookup"><span data-stu-id="b0cfd-113">-Location</span></span>
<span data-ttu-id="b0cfd-114">Especifica o local do centro de dados onde esse cmdlet cria o servidor.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-114">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="b0cfd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0cfd-115">-ResourceGroupName</span></span>
<span data-ttu-id="b0cfd-116">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o servidor.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-116">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="b0cfd-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b0cfd-117">-ServerName</span></span>
<span data-ttu-id="b0cfd-118">Especifica o nome do novo servidor.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-118">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="b0cfd-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b0cfd-119">-ServerVersion</span></span>
<span data-ttu-id="b0cfd-120">Especifica a versão do novo servidor.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-120">Specifies the version of the new server.</span></span> <span data-ttu-id="b0cfd-121">Os valores aceitáveis para esse parâmetro são: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="b0cfd-122">Especifique 2,0 para criar um servidor da versão 11 ou 12,0 para criar um servidor da versão 12.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-122">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="b0cfd-123">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="b0cfd-123">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="b0cfd-124">Especifica as credenciais de administrador do servidor de banco de dados SQL para o novo servidor.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-124">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="b0cfd-125">Para obter um objeto **PSCredential** , use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-125">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="b0cfd-126">Para obter mais informações, digite `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b0cfd-126">For more information, type `Get-Help
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

### <span data-ttu-id="b0cfd-127">-Marcas</span><span class="sxs-lookup"><span data-stu-id="b0cfd-127">-Tags</span></span>
<span data-ttu-id="b0cfd-128">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b0cfd-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b0cfd-129">For example:</span></span>

<span data-ttu-id="b0cfd-130">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b0cfd-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b0cfd-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0cfd-131">-Confirm</span></span>
<span data-ttu-id="b0cfd-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0cfd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0cfd-133">-WhatIf</span></span>
<span data-ttu-id="b0cfd-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0cfd-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0cfd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0cfd-136">-DefaultProfile</span></span>
<span data-ttu-id="b0cfd-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0cfd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0cfd-138">CommonParameters</span></span>
<span data-ttu-id="b0cfd-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0cfd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0cfd-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0cfd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0cfd-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0cfd-141">INPUTS</span></span>

## <span data-ttu-id="b0cfd-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0cfd-142">OUTPUTS</span></span>

### <span data-ttu-id="b0cfd-143">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b0cfd-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="b0cfd-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0cfd-144">NOTES</span></span>

## <span data-ttu-id="b0cfd-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0cfd-145">RELATED LINKS</span></span>

[<span data-ttu-id="b0cfd-146">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b0cfd-146">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="b0cfd-147">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b0cfd-147">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="b0cfd-148">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b0cfd-148">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="b0cfd-149">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0cfd-149">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b0cfd-150">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b0cfd-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
