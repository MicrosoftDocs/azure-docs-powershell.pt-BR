---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118626"
---
# <span data-ttu-id="7f096-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="7f096-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="7f096-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f096-102">SYNOPSIS</span></span>
<span data-ttu-id="7f096-103">Adiciona um Certificado de Criptografia de Dados Transparentes para uma determinada instância do SQL Server</span><span class="sxs-lookup"><span data-stu-id="7f096-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="7f096-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f096-104">SYNTAX</span></span>

### <span data-ttu-id="7f096-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7f096-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f096-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f096-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f096-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f096-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f096-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f096-108">DESCRIPTION</span></span>
<span data-ttu-id="7f096-109">A Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adiciona um Certificado de Criptografia de Dados Transparentes para uma determinada instância do SQL Server</span><span class="sxs-lookup"><span data-stu-id="7f096-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="7f096-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f096-110">EXAMPLES</span></span>

### <span data-ttu-id="7f096-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7f096-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="7f096-112">Adicionar certificado TDE a um servidor sql usando o nome do grupo de recursos e o nome do SQL Server</span><span class="sxs-lookup"><span data-stu-id="7f096-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="7f096-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7f096-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="7f096-114">Adicionar certificado TDE aos servidores usando o resourceId do servidor</span><span class="sxs-lookup"><span data-stu-id="7f096-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="7f096-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7f096-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="7f096-116">Adicionar certificado TDE a todos os servidores sql em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7f096-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="7f096-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f096-117">PARAMETERS</span></span>

### <span data-ttu-id="7f096-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f096-118">-DefaultProfile</span></span>
<span data-ttu-id="7f096-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f096-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f096-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f096-120">-PassThru</span></span>
<span data-ttu-id="7f096-121">Em Execução bem-sucedida, retorna o objeto de certificado que foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="7f096-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="7f096-122">-Senha</span><span class="sxs-lookup"><span data-stu-id="7f096-122">-Password</span></span>
<span data-ttu-id="7f096-123">A senha do certificado de criptografia de dados transparentes</span><span class="sxs-lookup"><span data-stu-id="7f096-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="7f096-124">-PrivateB ltd</span><span class="sxs-lookup"><span data-stu-id="7f096-124">-PrivateBlob</span></span>
<span data-ttu-id="7f096-125">O blob particular para certificado de criptografia de dados transparentes</span><span class="sxs-lookup"><span data-stu-id="7f096-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="7f096-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f096-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f096-127">O Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7f096-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="7f096-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f096-128">-ServerName</span></span>
<span data-ttu-id="7f096-129">O Nome do Servidor</span><span class="sxs-lookup"><span data-stu-id="7f096-129">The Server Name</span></span>

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

### <span data-ttu-id="7f096-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="7f096-130">-SqlServer</span></span>
<span data-ttu-id="7f096-131">O objeto de entrada do sql server</span><span class="sxs-lookup"><span data-stu-id="7f096-131">The sql server input object</span></span>

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

### <span data-ttu-id="7f096-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="7f096-132">-SqlServerResourceId</span></span>
<span data-ttu-id="7f096-133">A ID de recurso do sql Server</span><span class="sxs-lookup"><span data-stu-id="7f096-133">The sql server resource id</span></span>

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

### <span data-ttu-id="7f096-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7f096-134">-Confirm</span></span>
<span data-ttu-id="7f096-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f096-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f096-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f096-136">-WhatIf</span></span>
<span data-ttu-id="7f096-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7f096-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f096-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f096-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f096-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f096-139">CommonParameters</span></span>
<span data-ttu-id="7f096-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f096-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f096-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f096-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f096-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="7f096-142">INPUTS</span></span>

### <span data-ttu-id="7f096-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7f096-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="7f096-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7f096-144">System.String</span></span>

## <span data-ttu-id="7f096-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="7f096-145">OUTPUTS</span></span>

### <span data-ttu-id="7f096-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f096-146">System.Boolean</span></span>

## <span data-ttu-id="7f096-147">Notas</span><span class="sxs-lookup"><span data-stu-id="7f096-147">NOTES</span></span>

## <span data-ttu-id="7f096-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f096-148">RELATED LINKS</span></span>
