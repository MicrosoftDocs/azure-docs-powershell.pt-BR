---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427055"
---
# <span data-ttu-id="e9bd9-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="e9bd9-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="e9bd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bd9-103">Cria uma nova configuração do Active Directory para o Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="e9bd9-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="e9bd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9bd9-104">SYNTAX</span></span>

### <span data-ttu-id="e9bd9-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e9bd9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9bd9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9bd9-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9bd9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9bd9-107">DESCRIPTION</span></span>
<span data-ttu-id="e9bd9-108">O cmdlet **New-AzNetAppFilesActiveDirectory** cria uma nova configuração do Active Directory para uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="e9bd9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9bd9-109">EXAMPLES</span></span>

### <span data-ttu-id="e9bd9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9bd9-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="e9bd9-111">Esse comando obtém a senha do anúncio do promt em um secreates a nova configuração do Active Directory para a conta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="e9bd9-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="e9bd9-112">OS</span><span class="sxs-lookup"><span data-stu-id="e9bd9-112">PARAMETERS</span></span>

### <span data-ttu-id="e9bd9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e9bd9-113">-AccountName</span></span>
<span data-ttu-id="e9bd9-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="e9bd9-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="e9bd9-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="e9bd9-115">-AccountObject</span></span>
<span data-ttu-id="e9bd9-116">A conta para o novo objeto de política de backup</span><span class="sxs-lookup"><span data-stu-id="e9bd9-116">The Account for the new Backup Policy object</span></span>

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

### <span data-ttu-id="e9bd9-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="e9bd9-117">-AdName</span></span>
<span data-ttu-id="e9bd9-118">Nome do computador do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-118">Name of the active directory machine.</span></span>
<span data-ttu-id="e9bd9-119">Esse parâmetro opcional é usado apenas durante a criação do volume Kerberos</span><span class="sxs-lookup"><span data-stu-id="e9bd9-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="e9bd9-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="e9bd9-120">-BackupOperator</span></span>
<span data-ttu-id="e9bd9-121">Usuários a serem adicionados ao grupo interno de operadores de backup do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="e9bd9-122">Uma lista de nomes de dados exclusivos sem especificador de domínio</span><span class="sxs-lookup"><span data-stu-id="e9bd9-122">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="e9bd9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bd9-123">-DefaultProfile</span></span>
<span data-ttu-id="e9bd9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9bd9-125">-DNS</span><span class="sxs-lookup"><span data-stu-id="e9bd9-125">-Dns</span></span>
<span data-ttu-id="e9bd9-126">Lista separada por vírgulas de endereços IP de servidor DNS (IPv4 somente) para o domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="e9bd9-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="e9bd9-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="e9bd9-127">-Domain</span></span>
<span data-ttu-id="e9bd9-128">Nome do domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="e9bd9-128">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="e9bd9-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="e9bd9-129">-KdcIP</span></span>
<span data-ttu-id="e9bd9-130">endereços IP do servidor KDC para a máquina do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="e9bd9-131">Esse parâmetro opcional é usado apenas durante a criação do volume Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="e9bd9-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="e9bd9-132">-OrganizationalUnit</span></span>
<span data-ttu-id="e9bd9-133">A unidade organizacional (UO) dentro do Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="e9bd9-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="e9bd9-134">-Senha</span><span class="sxs-lookup"><span data-stu-id="e9bd9-134">-Password</span></span>
<span data-ttu-id="e9bd9-135">Senha de texto sem formatação do administrador de domínio do Active Directory; o valor é mascarado na resposta</span><span class="sxs-lookup"><span data-stu-id="e9bd9-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="e9bd9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9bd9-136">-ResourceGroupName</span></span>
<span data-ttu-id="e9bd9-137">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="e9bd9-137">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e9bd9-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="e9bd9-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="e9bd9-139">Quando o LDAP sobre SSL/TLS está habilitado, o cliente LDAP precisa ter o certificado da autoridade de certificação raiz autoassinado do serviço de certificado do Active Directory codificado na base64, esse parâmetro opcional é usado apenas para o protocolo duplo com volumes de mapeamento de usuário LDAP.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="e9bd9-140">-Site</span><span class="sxs-lookup"><span data-stu-id="e9bd9-140">-Site</span></span>
<span data-ttu-id="e9bd9-141">O site do Active Directory para o qual o serviço limitará a descoberta de controlador de domínio</span><span class="sxs-lookup"><span data-stu-id="e9bd9-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="e9bd9-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="e9bd9-142">-SmbServerName</span></span>
<span data-ttu-id="e9bd9-143">Nome NetBIOS do servidor SMB.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="e9bd9-144">Esse nome será registrado como uma conta de computador no anúncio e usado para montar volumes</span><span class="sxs-lookup"><span data-stu-id="e9bd9-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="e9bd9-145">-Username</span><span class="sxs-lookup"><span data-stu-id="e9bd9-145">-Username</span></span>
<span data-ttu-id="e9bd9-146">Nome de usuário do administrador de domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="e9bd9-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="e9bd9-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9bd9-147">-Confirm</span></span>
<span data-ttu-id="e9bd9-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9bd9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9bd9-149">-WhatIf</span></span>
<span data-ttu-id="e9bd9-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9bd9-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9bd9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bd9-152">CommonParameters</span></span>
<span data-ttu-id="e9bd9-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bd9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bd9-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9bd9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bd9-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9bd9-155">INPUTS</span></span>

### <span data-ttu-id="e9bd9-156">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e9bd9-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e9bd9-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9bd9-157">OUTPUTS</span></span>

### <span data-ttu-id="e9bd9-158">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="e9bd9-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="e9bd9-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9bd9-159">NOTES</span></span>

## <span data-ttu-id="e9bd9-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9bd9-160">RELATED LINKS</span></span>
