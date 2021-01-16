---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258597"
---
# <span data-ttu-id="a3a64-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a3a64-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a3a64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3a64-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a64-103">Atualiza uma configuração do Active Directory dos arquivos do Azure NetApp (ANF) para os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="a3a64-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="a3a64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3a64-104">SYNTAX</span></span>

### <span data-ttu-id="a3a64-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3a64-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a64-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3a64-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a64-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3a64-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3a64-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3a64-108">DESCRIPTION</span></span>
<span data-ttu-id="a3a64-109">O cmdlet **Update-AzNetAppFilesAccount** modifica uma configuração do Active Directory do ANF.</span><span class="sxs-lookup"><span data-stu-id="a3a64-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="a3a64-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3a64-110">EXAMPLES</span></span>

### <span data-ttu-id="a3a64-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3a64-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="a3a64-112">Esse comando executa uma atualização na configuração do Active Directory fornecida modificando o nome de usuário para o fornecido.</span><span class="sxs-lookup"><span data-stu-id="a3a64-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="a3a64-113">OS</span><span class="sxs-lookup"><span data-stu-id="a3a64-113">PARAMETERS</span></span>

### <span data-ttu-id="a3a64-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3a64-114">-AccountName</span></span>
<span data-ttu-id="a3a64-115">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="a3a64-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="a3a64-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="a3a64-116">-AccountObject</span></span>
<span data-ttu-id="a3a64-117">A conta para o objeto do Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3a64-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="a3a64-118">-ActiveDirectoryid</span><span class="sxs-lookup"><span data-stu-id="a3a64-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="a3a64-119">A ID do Active Directory do ANF</span><span class="sxs-lookup"><span data-stu-id="a3a64-119">The ID of the ANF active directory</span></span>

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

### <span data-ttu-id="a3a64-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="a3a64-120">-AdName</span></span>
<span data-ttu-id="a3a64-121">Nome do computador do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3a64-121">Name of the active directory machine.</span></span>
<span data-ttu-id="a3a64-122">Esse parâmetro opcional é usado apenas durante a criação do volume Kerberos</span><span class="sxs-lookup"><span data-stu-id="a3a64-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="a3a64-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="a3a64-123">-BackupOperator</span></span>
<span data-ttu-id="a3a64-124">Usuários a serem adicionados ao grupo interno de operadores de backup do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3a64-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="a3a64-125">Uma lista de nomes de dados exclusivos sem especificador de domínio</span><span class="sxs-lookup"><span data-stu-id="a3a64-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="a3a64-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a64-126">-DefaultProfile</span></span>
<span data-ttu-id="a3a64-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a64-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3a64-128">-DNS</span><span class="sxs-lookup"><span data-stu-id="a3a64-128">-Dns</span></span>
<span data-ttu-id="a3a64-129">Lista separada por vírgulas de endereços IP de servidor DNS (IPv4 somente) para o domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3a64-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="a3a64-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="a3a64-130">-Domain</span></span>
<span data-ttu-id="a3a64-131">Nome do domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3a64-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="a3a64-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3a64-132">-InputObject</span></span>
<span data-ttu-id="a3a64-133">O objeto do Active Directory a ser removido</span><span class="sxs-lookup"><span data-stu-id="a3a64-133">The active directory object to remove</span></span>

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

### <span data-ttu-id="a3a64-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="a3a64-134">-KdcIP</span></span>
<span data-ttu-id="a3a64-135">endereços IP do servidor KDC para a máquina do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3a64-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="a3a64-136">Esse parâmetro opcional é usado apenas durante a criação do volume Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a3a64-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="a3a64-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="a3a64-137">-OrganizationalUnit</span></span>
<span data-ttu-id="a3a64-138">A unidade organizacional (UO) dentro do Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3a64-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="a3a64-139">-Senha</span><span class="sxs-lookup"><span data-stu-id="a3a64-139">-Password</span></span>
<span data-ttu-id="a3a64-140">Senha de texto sem formatação do administrador de domínio do Active Directory; o valor é mascarado na resposta</span><span class="sxs-lookup"><span data-stu-id="a3a64-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="a3a64-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a64-141">-ResourceGroupName</span></span>
<span data-ttu-id="a3a64-142">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="a3a64-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a3a64-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="a3a64-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="a3a64-144">Quando o LDAP sobre SSL/TLS está habilitado, o cliente LDAP precisa ter o certificado da autoridade de certificação raiz autoassinado do serviço de certificado do Active Directory codificado na base64, esse parâmetro opcional é usado apenas para o protocolo duplo com volumes de mapeamento de usuário LDAP.</span><span class="sxs-lookup"><span data-stu-id="a3a64-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="a3a64-145">-Site</span><span class="sxs-lookup"><span data-stu-id="a3a64-145">-Site</span></span>
<span data-ttu-id="a3a64-146">O site do Active Directory para o qual o serviço limitará a descoberta de controlador de domínio</span><span class="sxs-lookup"><span data-stu-id="a3a64-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="a3a64-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="a3a64-147">-SmbServerName</span></span>
<span data-ttu-id="a3a64-148">Nome NetBIOS do servidor SMB.</span><span class="sxs-lookup"><span data-stu-id="a3a64-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="a3a64-149">Esse nome será registrado como uma conta de computador no anúncio e usado para montar volumes</span><span class="sxs-lookup"><span data-stu-id="a3a64-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="a3a64-150">-Username</span><span class="sxs-lookup"><span data-stu-id="a3a64-150">-Username</span></span>
<span data-ttu-id="a3a64-151">Nome de usuário do administrador de domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3a64-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="a3a64-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3a64-152">-Confirm</span></span>
<span data-ttu-id="a3a64-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3a64-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3a64-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3a64-154">-WhatIf</span></span>
<span data-ttu-id="a3a64-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3a64-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3a64-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3a64-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3a64-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a64-157">CommonParameters</span></span>
<span data-ttu-id="a3a64-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a64-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a64-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3a64-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a64-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3a64-160">INPUTS</span></span>

### <span data-ttu-id="a3a64-161">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a3a64-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="a3a64-162">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a3a64-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a3a64-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3a64-163">OUTPUTS</span></span>

### <span data-ttu-id="a3a64-164">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a3a64-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a3a64-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3a64-165">NOTES</span></span>

## <span data-ttu-id="a3a64-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3a64-166">RELATED LINKS</span></span>
