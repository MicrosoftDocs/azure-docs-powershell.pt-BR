---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 333de53ccd3632188100af7f3fcde10e140537c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431896"
---
# <span data-ttu-id="b0dd3-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b0dd3-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="b0dd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="b0dd3-103">Adiciona um certificado de criptografia de dados transparente para a instância do SQL Server fornecida</span><span class="sxs-lookup"><span data-stu-id="b0dd3-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0dd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0dd3-104">SYNTAX</span></span>

### <span data-ttu-id="b0dd3-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0dd3-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0dd3-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0dd3-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0dd3-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0dd3-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0dd3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0dd3-108">DESCRIPTION</span></span>
<span data-ttu-id="b0dd3-109">O Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adiciona um certificado de criptografia de dados transparente para a instância do SQL Server fornecida</span><span class="sxs-lookup"><span data-stu-id="b0dd3-109">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="b0dd3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0dd3-110">EXAMPLES</span></span>

### <span data-ttu-id="b0dd3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b0dd3-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="b0dd3-112">Adicionar o certificado TDE a um SQL Server usando o nome do grupo de recursos e o nome do SQL Server</span><span class="sxs-lookup"><span data-stu-id="b0dd3-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="b0dd3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b0dd3-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzureRmSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="b0dd3-114">Adicionar certificado TDE aos servidores usando o ResourceId do servidor</span><span class="sxs-lookup"><span data-stu-id="b0dd3-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="b0dd3-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b0dd3-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzureRmSqlServer | Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="b0dd3-116">Adicionar certificado do TDE a todos os SQL Servers em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b0dd3-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="b0dd3-117">OS</span><span class="sxs-lookup"><span data-stu-id="b0dd3-117">PARAMETERS</span></span>

### <span data-ttu-id="b0dd3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0dd3-118">-DefaultProfile</span></span>
<span data-ttu-id="b0dd3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0dd3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0dd3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0dd3-120">-PassThru</span></span>
<span data-ttu-id="b0dd3-121">Na execução bem-sucedida, retorna o objeto de certificado que foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="b0dd3-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="b0dd3-122">-Senha</span><span class="sxs-lookup"><span data-stu-id="b0dd3-122">-Password</span></span>
<span data-ttu-id="b0dd3-123">A senha para certificado de criptografia de dados transparente</span><span class="sxs-lookup"><span data-stu-id="b0dd3-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="b0dd3-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="b0dd3-124">-PrivateBlob</span></span>
<span data-ttu-id="b0dd3-125">O blob privado para certificado de criptografia de dados transparente</span><span class="sxs-lookup"><span data-stu-id="b0dd3-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="b0dd3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0dd3-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0dd3-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b0dd3-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="b0dd3-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b0dd3-128">-ServerName</span></span>
<span data-ttu-id="b0dd3-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="b0dd3-129">The Server Name</span></span>

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

### <span data-ttu-id="b0dd3-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="b0dd3-130">-SqlServer</span></span>
<span data-ttu-id="b0dd3-131">O objeto de entrada do SQL Server</span><span class="sxs-lookup"><span data-stu-id="b0dd3-131">The sql server input object</span></span>

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

### <span data-ttu-id="b0dd3-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="b0dd3-132">-SqlServerResourceId</span></span>
<span data-ttu-id="b0dd3-133">A ID de recurso do SQL Server</span><span class="sxs-lookup"><span data-stu-id="b0dd3-133">The sql server resource id</span></span>

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

### <span data-ttu-id="b0dd3-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0dd3-134">-Confirm</span></span>
<span data-ttu-id="b0dd3-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0dd3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0dd3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0dd3-136">-WhatIf</span></span>
<span data-ttu-id="b0dd3-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0dd3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0dd3-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0dd3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0dd3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0dd3-139">CommonParameters</span></span>
<span data-ttu-id="b0dd3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0dd3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0dd3-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0dd3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0dd3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0dd3-142">INPUTS</span></span>

### <span data-ttu-id="b0dd3-143">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b0dd3-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="b0dd3-144">Parâmetros: SqlServer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0dd3-144">Parameters: SqlServer (ByValue)</span></span>

### <span data-ttu-id="b0dd3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b0dd3-145">System.String</span></span>

## <span data-ttu-id="b0dd3-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0dd3-146">OUTPUTS</span></span>

### <span data-ttu-id="b0dd3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0dd3-147">System.Boolean</span></span>

## <span data-ttu-id="b0dd3-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0dd3-148">NOTES</span></span>

## <span data-ttu-id="b0dd3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0dd3-149">RELATED LINKS</span></span>
