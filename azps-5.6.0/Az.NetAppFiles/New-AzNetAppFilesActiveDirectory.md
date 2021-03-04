---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 73d0ae2a4f4595024db3ee5553a446a5832f0476
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887447"
---
# <span data-ttu-id="6d014-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="6d014-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="6d014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d014-102">SYNOPSIS</span></span>
<span data-ttu-id="6d014-103">Cria uma nova configuração do Active Directory Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="6d014-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="6d014-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6d014-104">SYNTAX</span></span>

### <span data-ttu-id="6d014-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d014-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d014-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d014-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d014-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d014-107">DESCRIPTION</span></span>
<span data-ttu-id="6d014-108">O cmdlet **New-AzNetAppFilesActiveDirectory** cria uma nova configuração do active directory para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="6d014-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="6d014-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d014-109">EXAMPLES</span></span>

### <span data-ttu-id="6d014-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d014-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="6d014-111">Esse comando obtém a senha do AD de promt em uma secreta a nova configuração do Active Directory para a conta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="6d014-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="6d014-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6d014-112">PARAMETERS</span></span>

### <span data-ttu-id="6d014-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d014-113">-AccountName</span></span>
<span data-ttu-id="6d014-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="6d014-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="6d014-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6d014-115">-AccountObject</span></span>
<span data-ttu-id="6d014-116">A Conta do novo objeto de Política de Backup</span><span class="sxs-lookup"><span data-stu-id="6d014-116">The Account for the new Backup Policy object</span></span>

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

### <span data-ttu-id="6d014-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="6d014-117">-AdName</span></span>
<span data-ttu-id="6d014-118">Nome do computador do active directory.</span><span class="sxs-lookup"><span data-stu-id="6d014-118">Name of the active directory machine.</span></span>
<span data-ttu-id="6d014-119">Esse parâmetro opcional é usado somente durante a criação de volume kerberos</span><span class="sxs-lookup"><span data-stu-id="6d014-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="6d014-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="6d014-120">-BackupOperator</span></span>
<span data-ttu-id="6d014-121">Usuários a serem adicionados ao grupo de diretório ativo Operador de Backup Integrado.</span><span class="sxs-lookup"><span data-stu-id="6d014-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="6d014-122">Uma lista de nomes de usuário exclusivos sem um especificador de domínio</span><span class="sxs-lookup"><span data-stu-id="6d014-122">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="6d014-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d014-123">-DefaultProfile</span></span>
<span data-ttu-id="6d014-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d014-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d014-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="6d014-125">-Dns</span></span>
<span data-ttu-id="6d014-126">Lista separada por vírgulas de endereços IP do servidor DNS (somente IPv4) para o domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d014-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="6d014-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="6d014-127">-Domain</span></span>
<span data-ttu-id="6d014-128">Nome do domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d014-128">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="6d014-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="6d014-129">-KdcIP</span></span>
<span data-ttu-id="6d014-130">Endereços IP do servidor kdc para o computador do active directory.</span><span class="sxs-lookup"><span data-stu-id="6d014-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="6d014-131">Esse parâmetro opcional é usado apenas durante a criação de volume kerberos.</span><span class="sxs-lookup"><span data-stu-id="6d014-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="6d014-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="6d014-132">-OrganizationalUnit</span></span>
<span data-ttu-id="6d014-133">A Unidade Organizacional (UO) no Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d014-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="6d014-134">-Password</span><span class="sxs-lookup"><span data-stu-id="6d014-134">-Password</span></span>
<span data-ttu-id="6d014-135">Senha de texto simples do administrador de domínio do Active Directory, o valor é mascarado na resposta</span><span class="sxs-lookup"><span data-stu-id="6d014-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="6d014-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d014-136">-ResourceGroupName</span></span>
<span data-ttu-id="6d014-137">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="6d014-137">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="6d014-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="6d014-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="6d014-139">Quando o LDAP sobre SSL/TLS está habilitado, o cliente LDAP é necessário para ter o certificado de AC raiz auto-assinado do Serviço de Certificado do Active Directory base64, esse parâmetro opcional é usado apenas para protocolo dual com volumes de mapeamento de usuário LDAP.</span><span class="sxs-lookup"><span data-stu-id="6d014-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="6d014-140">-Site</span><span class="sxs-lookup"><span data-stu-id="6d014-140">-Site</span></span>
<span data-ttu-id="6d014-141">O site do Active Directory para o qual o serviço limitará a descoberta do Controlador de Domínio</span><span class="sxs-lookup"><span data-stu-id="6d014-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="6d014-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="6d014-142">-SmbServerName</span></span>
<span data-ttu-id="6d014-143">Nome NetBIOS do servidor SMB.</span><span class="sxs-lookup"><span data-stu-id="6d014-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="6d014-144">Esse nome será registrado como uma conta de computador no AD e usado para montar volumes</span><span class="sxs-lookup"><span data-stu-id="6d014-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="6d014-145">-Username</span><span class="sxs-lookup"><span data-stu-id="6d014-145">-Username</span></span>
<span data-ttu-id="6d014-146">Nome de usuário do administrador de domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d014-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="6d014-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d014-147">-Confirm</span></span>
<span data-ttu-id="6d014-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d014-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d014-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d014-149">-WhatIf</span></span>
<span data-ttu-id="6d014-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d014-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d014-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d014-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d014-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d014-152">CommonParameters</span></span>
<span data-ttu-id="6d014-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d014-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d014-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d014-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d014-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d014-155">INPUTS</span></span>

### <span data-ttu-id="6d014-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6d014-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6d014-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6d014-157">OUTPUTS</span></span>

### <span data-ttu-id="6d014-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="6d014-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="6d014-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="6d014-159">NOTES</span></span>

## <span data-ttu-id="6d014-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d014-160">RELATED LINKS</span></span>
