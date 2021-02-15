---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112931"
---
# <span data-ttu-id="158e6-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="158e6-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="158e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="158e6-102">SYNOPSIS</span></span>
<span data-ttu-id="158e6-103">Cria uma nova configuração do Azure NetApp Files (ANF) active directory.</span><span class="sxs-lookup"><span data-stu-id="158e6-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="158e6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="158e6-104">SYNTAX</span></span>

### <span data-ttu-id="158e6-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="158e6-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="158e6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="158e6-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="158e6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="158e6-107">DESCRIPTION</span></span>
<span data-ttu-id="158e6-108">O cmdlet **New-AzNetAppFilesActiveDirectory** cria uma nova configuração do Active Directory para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="158e6-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="158e6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="158e6-109">EXAMPLES</span></span>

### <span data-ttu-id="158e6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="158e6-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="158e6-111">Esse comando obtém a senha do AD de um comando em uma nova configuração do Active Directory para a conta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="158e6-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="158e6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="158e6-112">PARAMETERS</span></span>

### <span data-ttu-id="158e6-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="158e6-113">-AccountName</span></span>
<span data-ttu-id="158e6-114">O nome da conta da ANF</span><span class="sxs-lookup"><span data-stu-id="158e6-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="158e6-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="158e6-115">-AccountObject</span></span>
<span data-ttu-id="158e6-116">A Conta do novo objeto de Política de Backup</span><span class="sxs-lookup"><span data-stu-id="158e6-116">The Account for the new Backup Policy object</span></span>

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

### <span data-ttu-id="158e6-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="158e6-117">-AdName</span></span>
<span data-ttu-id="158e6-118">Nome do computador do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="158e6-118">Name of the active directory machine.</span></span>
<span data-ttu-id="158e6-119">Este parâmetro opcional é usado apenas durante a criação de volume kerberos</span><span class="sxs-lookup"><span data-stu-id="158e6-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="158e6-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="158e6-120">-BackupOperator</span></span>
<span data-ttu-id="158e6-121">Usuários a serem adicionados ao grupo Do Operador de Backup Integrado do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="158e6-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="158e6-122">Uma lista de nomes de usuário exclusivos sem o especificador de domínio</span><span class="sxs-lookup"><span data-stu-id="158e6-122">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="158e6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158e6-123">-DefaultProfile</span></span>
<span data-ttu-id="158e6-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="158e6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="158e6-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="158e6-125">-Dns</span></span>
<span data-ttu-id="158e6-126">Lista separada por vírgulas de endereços IP do servidor DNS (somente IPv4) para o domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="158e6-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="158e6-127">-Domínio</span><span class="sxs-lookup"><span data-stu-id="158e6-127">-Domain</span></span>
<span data-ttu-id="158e6-128">Nome do domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="158e6-128">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="158e6-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="158e6-129">-KdcIP</span></span>
<span data-ttu-id="158e6-130">endereços IP do servidor kdc para o computador active directory.</span><span class="sxs-lookup"><span data-stu-id="158e6-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="158e6-131">Esse parâmetro opcional é usado apenas durante a criação de volume kerberos.</span><span class="sxs-lookup"><span data-stu-id="158e6-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="158e6-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="158e6-132">-OrganizationalUnit</span></span>
<span data-ttu-id="158e6-133">A Unidade Organizacional (OU) no Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="158e6-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="158e6-134">-Senha</span><span class="sxs-lookup"><span data-stu-id="158e6-134">-Password</span></span>
<span data-ttu-id="158e6-135">Senha de texto sem texto do administrador de domínio do Active Directory, o valor é mascarado na resposta</span><span class="sxs-lookup"><span data-stu-id="158e6-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="158e6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="158e6-136">-ResourceGroupName</span></span>
<span data-ttu-id="158e6-137">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="158e6-137">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="158e6-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="158e6-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="158e6-139">Quando a LDAP sobre SSL/TLS está habilitada, o cliente LDAP é necessário para ter o certificado de AC raiz do Active Directory auto-assinado do Serviço de Certificado do Active Directory codificado, esse parâmetro opcional é usado somente para protocolo duplo com volumes de mapeamento de usuário LDAP.</span><span class="sxs-lookup"><span data-stu-id="158e6-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="158e6-140">-Site</span><span class="sxs-lookup"><span data-stu-id="158e6-140">-Site</span></span>
<span data-ttu-id="158e6-141">O site do Active Directory para o qual o serviço limitará a descoberta do Controlador de Domínio</span><span class="sxs-lookup"><span data-stu-id="158e6-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="158e6-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="158e6-142">-SmbServerName</span></span>
<span data-ttu-id="158e6-143">Nome netBIOS do servidor SMB.</span><span class="sxs-lookup"><span data-stu-id="158e6-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="158e6-144">Esse nome será registrado como uma conta de computador no AD e usado para montar volumes</span><span class="sxs-lookup"><span data-stu-id="158e6-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="158e6-145">-Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="158e6-145">-Username</span></span>
<span data-ttu-id="158e6-146">Nome de usuário do administrador de domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="158e6-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="158e6-147">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="158e6-147">-Confirm</span></span>
<span data-ttu-id="158e6-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="158e6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="158e6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="158e6-149">-WhatIf</span></span>
<span data-ttu-id="158e6-150">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="158e6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="158e6-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="158e6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="158e6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158e6-152">CommonParameters</span></span>
<span data-ttu-id="158e6-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158e6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158e6-154">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="158e6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158e6-155">Entradas</span><span class="sxs-lookup"><span data-stu-id="158e6-155">INPUTS</span></span>

### <span data-ttu-id="158e6-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="158e6-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="158e6-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="158e6-157">OUTPUTS</span></span>

### <span data-ttu-id="158e6-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="158e6-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="158e6-159">Notas</span><span class="sxs-lookup"><span data-stu-id="158e6-159">NOTES</span></span>

## <span data-ttu-id="158e6-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="158e6-160">RELATED LINKS</span></span>
