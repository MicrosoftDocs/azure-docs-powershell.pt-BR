---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946048"
---
# <span data-ttu-id="d7dc8-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d7dc8-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="d7dc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="d7dc8-103">Habilita uma extensão de domínio do anúncio para um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="d7dc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7dc8-104">SYNTAX</span></span>

### <span data-ttu-id="d7dc8-105">JoinDomainUsingEnumOptions (padrão)</span><span class="sxs-lookup"><span data-stu-id="d7dc8-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7dc8-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="d7dc8-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7dc8-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="d7dc8-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7dc8-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="d7dc8-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7dc8-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="d7dc8-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7dc8-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="d7dc8-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d7dc8-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7dc8-111">DESCRIPTION</span></span>
<span data-ttu-id="d7dc8-112">O cmdlet **set-AzureServiceADDomainExtension** habilita uma extensão de domínio AD (Active Directory) para um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="d7dc8-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7dc8-113">EXAMPLES</span></span>

### <span data-ttu-id="d7dc8-114">1:</span><span class="sxs-lookup"><span data-stu-id="d7dc8-114">1:</span></span>
```

```

## <span data-ttu-id="d7dc8-115">OS</span><span class="sxs-lookup"><span data-stu-id="d7dc8-115">PARAMETERS</span></span>

### <span data-ttu-id="d7dc8-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="d7dc8-116">-CertificateThumbprint</span></span>
<span data-ttu-id="d7dc8-117">Especifica uma impressão digital de certificado a ser usada para criptografar a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="d7dc8-118">Este certificado já existe no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="d7dc8-119">Se você não especificar um certificado, esse cmdlet criará um certificado.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-120">-Credential</span><span class="sxs-lookup"><span data-stu-id="d7dc8-120">-Credential</span></span>
<span data-ttu-id="d7dc8-121">Especifica as credenciais para ingressar no domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="d7dc8-122">As credenciais incluem um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-123">-DomainName</span><span class="sxs-lookup"><span data-stu-id="d7dc8-123">-DomainName</span></span>
<span data-ttu-id="d7dc8-124">Especifica o nome de domínio do anúncio.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="d7dc8-125">-ExtensionId</span></span>
<span data-ttu-id="d7dc8-126">Especifica a ID de extensão.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d7dc8-127">-InformationAction</span></span>
<span data-ttu-id="d7dc8-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d7dc8-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d7dc8-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7dc8-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="d7dc8-130">Continue</span></span>
- <span data-ttu-id="d7dc8-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="d7dc8-131">Ignore</span></span>
- <span data-ttu-id="d7dc8-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="d7dc8-132">Inquire</span></span>
- <span data-ttu-id="d7dc8-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d7dc8-133">SilentlyContinue</span></span>
- <span data-ttu-id="d7dc8-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="d7dc8-134">Stop</span></span>
- <span data-ttu-id="d7dc8-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="d7dc8-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d7dc8-136">-InformationVariable</span></span>
<span data-ttu-id="d7dc8-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="d7dc8-138">-JoinOption</span></span>
<span data-ttu-id="d7dc8-139">Especifica a enumeração da opção de junção.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-140">-Opções</span><span class="sxs-lookup"><span data-stu-id="d7dc8-140">-Options</span></span>
<span data-ttu-id="d7dc8-141">Especifica a opção de junção de inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="d7dc8-142">-OUPath</span></span>
<span data-ttu-id="d7dc8-143">Especifica o caminho da unidade organizacional (UO) para a operação de ingresso no domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-144">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d7dc8-144">-Profile</span></span>
<span data-ttu-id="d7dc8-145">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7dc8-146">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-147">-Restart</span><span class="sxs-lookup"><span data-stu-id="d7dc8-147">-Restart</span></span>
<span data-ttu-id="d7dc8-148">Especifica se o computador deve ser reiniciado se a operação de ingresso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-149">-Função</span><span class="sxs-lookup"><span data-stu-id="d7dc8-149">-Role</span></span>
<span data-ttu-id="d7dc8-150">Especifica uma matriz opcional de funções para as quais especificar a configuração da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="d7dc8-151">Se não especificado, a configuração de domínio do AD será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-152">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d7dc8-152">-ServiceName</span></span>
<span data-ttu-id="d7dc8-153">Especifica o nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-153">Specifies the cloud service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-154">-Slot</span><span class="sxs-lookup"><span data-stu-id="d7dc8-154">-Slot</span></span>
<span data-ttu-id="d7dc8-155">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="d7dc8-156">Os valores aceitáveis para esse parâmetro são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-156">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="d7dc8-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="d7dc8-158">Especifica um algoritmo de hash de impressão digital que é usado com a impressão digital para identificar o certificado.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="d7dc8-159">Esse parâmetro é opcional, e o padrão é SHA1.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="d7dc8-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="d7dc8-161">Especifica as credenciais (nome de usuário e senha) para sair do domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-162">-Versão</span><span class="sxs-lookup"><span data-stu-id="d7dc8-162">-Version</span></span>
<span data-ttu-id="d7dc8-163">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-164">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="d7dc8-164">-WorkgroupName</span></span>
<span data-ttu-id="d7dc8-165">Especifica o nome do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="d7dc8-166">-X509Certificate</span></span>
<span data-ttu-id="d7dc8-167">Especifica um certificado X509 que quando especificado será carregado automaticamente para o serviço de nuvem e usado para criptografar a configuração privada de extensão.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dc8-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7dc8-168">CommonParameters</span></span>
<span data-ttu-id="d7dc8-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7dc8-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7dc8-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7dc8-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7dc8-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7dc8-171">INPUTS</span></span>

## <span data-ttu-id="d7dc8-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7dc8-172">OUTPUTS</span></span>

## <span data-ttu-id="d7dc8-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7dc8-173">NOTES</span></span>

## <span data-ttu-id="d7dc8-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7dc8-174">RELATED LINKS</span></span>

[<span data-ttu-id="d7dc8-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d7dc8-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="d7dc8-176">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d7dc8-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="d7dc8-177">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="d7dc8-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


