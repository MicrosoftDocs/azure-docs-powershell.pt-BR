---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: beb51449ea0264defe640ba60ad687be405ab669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886567"
---
# <span data-ttu-id="b7436-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b7436-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="b7436-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7436-102">SYNOPSIS</span></span>
<span data-ttu-id="b7436-103">Adiciona um Certificado de Criptografia de Dados Transparente para a instância SQL Server determinada</span><span class="sxs-lookup"><span data-stu-id="b7436-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="b7436-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7436-104">SYNTAX</span></span>

### <span data-ttu-id="b7436-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b7436-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7436-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7436-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7436-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7436-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7436-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7436-108">DESCRIPTION</span></span>
<span data-ttu-id="b7436-109">O Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adiciona um Certificado de Criptografia de Dados Transparente para a instância SQL Server determinada</span><span class="sxs-lookup"><span data-stu-id="b7436-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="b7436-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7436-110">EXAMPLES</span></span>

### <span data-ttu-id="b7436-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7436-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="b7436-112">Adicionar certificado TDE a um servidor sql usando o nome do grupo de recursos e SQL Server nome</span><span class="sxs-lookup"><span data-stu-id="b7436-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="b7436-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b7436-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="b7436-114">Adicionar certificado TDE aos servidores usando resourceId do servidor</span><span class="sxs-lookup"><span data-stu-id="b7436-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="b7436-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b7436-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="b7436-116">Adicionar certificado TDE a todos os servidores sql em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b7436-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="b7436-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7436-117">PARAMETERS</span></span>

### <span data-ttu-id="b7436-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7436-118">-DefaultProfile</span></span>
<span data-ttu-id="b7436-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7436-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7436-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7436-120">-PassThru</span></span>
<span data-ttu-id="b7436-121">Em Execução bem-sucedida, retorna o objeto certificate que foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="b7436-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="b7436-122">-Password</span><span class="sxs-lookup"><span data-stu-id="b7436-122">-Password</span></span>
<span data-ttu-id="b7436-123">A senha para certificado de criptografia de dados transparentes</span><span class="sxs-lookup"><span data-stu-id="b7436-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7436-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="b7436-124">-PrivateBlob</span></span>
<span data-ttu-id="b7436-125">O blob privado para certificado de criptografia de dados transparente</span><span class="sxs-lookup"><span data-stu-id="b7436-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7436-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7436-126">-ResourceGroupName</span></span>
<span data-ttu-id="b7436-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b7436-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7436-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7436-128">-ServerName</span></span>
<span data-ttu-id="b7436-129">O Nome do Servidor</span><span class="sxs-lookup"><span data-stu-id="b7436-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7436-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="b7436-130">-SqlServer</span></span>
<span data-ttu-id="b7436-131">O objeto de entrada do sql Server</span><span class="sxs-lookup"><span data-stu-id="b7436-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7436-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="b7436-132">-SqlServerResourceId</span></span>
<span data-ttu-id="b7436-133">A id de recurso do sql Server</span><span class="sxs-lookup"><span data-stu-id="b7436-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7436-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7436-134">-Confirm</span></span>
<span data-ttu-id="b7436-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7436-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7436-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7436-136">-WhatIf</span></span>
<span data-ttu-id="b7436-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7436-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7436-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7436-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7436-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7436-139">CommonParameters</span></span>
<span data-ttu-id="b7436-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7436-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7436-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7436-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7436-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7436-142">INPUTS</span></span>

### <span data-ttu-id="b7436-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b7436-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="b7436-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b7436-144">System.String</span></span>

## <span data-ttu-id="b7436-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7436-145">OUTPUTS</span></span>

### <span data-ttu-id="b7436-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7436-146">System.Boolean</span></span>

## <span data-ttu-id="b7436-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7436-147">NOTES</span></span>

## <span data-ttu-id="b7436-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7436-148">RELATED LINKS</span></span>
