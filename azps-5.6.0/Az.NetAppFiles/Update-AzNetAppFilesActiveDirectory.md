---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 3baa4a20d6109d2767dee1b4ff53e2b363adfccf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887403"
---
# <span data-ttu-id="6fdd3-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="6fdd3-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="6fdd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fdd3-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdd3-103">Atualiza uma configuração do active directory Azure NetApp Files (ANF) para os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="6fdd3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6fdd3-104">SYNTAX</span></span>

### <span data-ttu-id="6fdd3-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6fdd3-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fdd3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fdd3-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fdd3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fdd3-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fdd3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6fdd3-108">DESCRIPTION</span></span>
<span data-ttu-id="6fdd3-109">O cmdlet **Update-AzNetAppFilesAccount** modifica uma configuração do active directory ANF.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="6fdd3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fdd3-110">EXAMPLES</span></span>

### <span data-ttu-id="6fdd3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6fdd3-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="6fdd3-112">Este comando executa uma atualização na configuração determinada do active directory modificando o nome de usuário para o fornecido.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="6fdd3-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6fdd3-113">PARAMETERS</span></span>

### <span data-ttu-id="6fdd3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6fdd3-114">-AccountName</span></span>
<span data-ttu-id="6fdd3-115">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="6fdd3-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd3-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6fdd3-116">-AccountObject</span></span>
<span data-ttu-id="6fdd3-117">A conta do objeto active directory</span><span class="sxs-lookup"><span data-stu-id="6fdd3-117">The account for the active directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd3-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="6fdd3-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="6fdd3-119">A ID do active directory ANF</span><span class="sxs-lookup"><span data-stu-id="6fdd3-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd3-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="6fdd3-120">-AdName</span></span>
<span data-ttu-id="6fdd3-121">Nome do computador do active directory.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-121">Name of the active directory machine.</span></span>
<span data-ttu-id="6fdd3-122">Esse parâmetro opcional é usado somente durante a criação de volume kerberos</span><span class="sxs-lookup"><span data-stu-id="6fdd3-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="6fdd3-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="6fdd3-123">-BackupOperator</span></span>
<span data-ttu-id="6fdd3-124">Usuários a serem adicionados ao grupo de diretório ativo Operador de Backup Integrado.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="6fdd3-125">Uma lista de nomes de usuário exclusivos sem um especificador de domínio</span><span class="sxs-lookup"><span data-stu-id="6fdd3-125">A list of unique usernames without domain specifier</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdd3-126">-DefaultProfile</span></span>
<span data-ttu-id="6fdd3-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fdd3-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="6fdd3-128">-Dns</span></span>
<span data-ttu-id="6fdd3-129">Lista separada por vírgulas de endereços IP do servidor DNS (somente IPv4) para o domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="6fdd3-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd3-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="6fdd3-130">-Domain</span></span>
<span data-ttu-id="6fdd3-131">Nome do domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="6fdd3-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="6fdd3-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fdd3-132">-InputObject</span></span>
<span data-ttu-id="6fdd3-133">O objeto active directory a ser removido</span><span class="sxs-lookup"><span data-stu-id="6fdd3-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd3-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="6fdd3-134">-KdcIP</span></span>
<span data-ttu-id="6fdd3-135">Endereços IP do servidor kdc para o computador do active directory.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="6fdd3-136">Esse parâmetro opcional é usado apenas durante a criação de volume kerberos.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="6fdd3-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="6fdd3-137">-OrganizationalUnit</span></span>
<span data-ttu-id="6fdd3-138">A Unidade Organizacional (UO) no Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="6fdd3-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="6fdd3-139">-Password</span><span class="sxs-lookup"><span data-stu-id="6fdd3-139">-Password</span></span>
<span data-ttu-id="6fdd3-140">Senha de texto simples do administrador de domínio do Active Directory, o valor é mascarado na resposta</span><span class="sxs-lookup"><span data-stu-id="6fdd3-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="6fdd3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fdd3-141">-ResourceGroupName</span></span>
<span data-ttu-id="6fdd3-142">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="6fdd3-142">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd3-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="6fdd3-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="6fdd3-144">Quando o LDAP sobre SSL/TLS está habilitado, o cliente LDAP é necessário para ter o certificado de AC raiz auto-assinado do Serviço de Certificado do Active Directory base64, esse parâmetro opcional é usado apenas para protocolo dual com volumes de mapeamento de usuário LDAP.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="6fdd3-145">-Site</span><span class="sxs-lookup"><span data-stu-id="6fdd3-145">-Site</span></span>
<span data-ttu-id="6fdd3-146">O site do Active Directory para o qual o serviço limitará a descoberta do Controlador de Domínio</span><span class="sxs-lookup"><span data-stu-id="6fdd3-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="6fdd3-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="6fdd3-147">-SmbServerName</span></span>
<span data-ttu-id="6fdd3-148">Nome NetBIOS do servidor SMB.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="6fdd3-149">Esse nome será registrado como uma conta de computador no AD e usado para montar volumes</span><span class="sxs-lookup"><span data-stu-id="6fdd3-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="6fdd3-150">-Username</span><span class="sxs-lookup"><span data-stu-id="6fdd3-150">-Username</span></span>
<span data-ttu-id="6fdd3-151">Nome de usuário do administrador de domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="6fdd3-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="6fdd3-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fdd3-152">-Confirm</span></span>
<span data-ttu-id="6fdd3-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fdd3-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fdd3-154">-WhatIf</span></span>
<span data-ttu-id="6fdd3-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fdd3-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fdd3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdd3-157">CommonParameters</span></span>
<span data-ttu-id="6fdd3-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fdd3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdd3-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fdd3-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdd3-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fdd3-160">INPUTS</span></span>

### <span data-ttu-id="6fdd3-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6fdd3-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="6fdd3-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="6fdd3-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="6fdd3-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6fdd3-163">OUTPUTS</span></span>

### <span data-ttu-id="6fdd3-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="6fdd3-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="6fdd3-165">NOTES</span><span class="sxs-lookup"><span data-stu-id="6fdd3-165">NOTES</span></span>

## <span data-ttu-id="6fdd3-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fdd3-166">RELATED LINKS</span></span>
