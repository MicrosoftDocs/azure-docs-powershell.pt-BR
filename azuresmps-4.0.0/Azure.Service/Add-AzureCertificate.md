---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946395"
---
# <span data-ttu-id="b57a6-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b57a6-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="b57a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b57a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b57a6-103">Carrega um certificado para um serviço de nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="b57a6-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="b57a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b57a6-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b57a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b57a6-105">DESCRIPTION</span></span>
<span data-ttu-id="b57a6-106">O cmdlet **Add-AzureCertificate** carrega um certificado para um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="b57a6-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="b57a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b57a6-107">EXAMPLES</span></span>

### <span data-ttu-id="b57a6-108">Exemplo 1: carregar um certificado e uma senha</span><span class="sxs-lookup"><span data-stu-id="b57a6-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="b57a6-109">Esse comando carrega o arquivo de certificado ContosoCertificate. pfx para um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b57a6-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="b57a6-110">O comando especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="b57a6-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="b57a6-111">Exemplo 2: carregar um arquivo de certificado</span><span class="sxs-lookup"><span data-stu-id="b57a6-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="b57a6-112">Esse comando carrega o arquivo de certificado ContosoCertificate. cer para um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b57a6-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="b57a6-113">O comando especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="b57a6-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="b57a6-114">Exemplo 3: carregar um objeto de certificado</span><span class="sxs-lookup"><span data-stu-id="b57a6-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="b57a6-115">O primeiro comando obtém um certificado do meu repositório de um usuário usando o cmdlet **Get-Item** básico do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b57a6-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="b57a6-116">O comando armazena o certificado na variável $Certificate.</span><span class="sxs-lookup"><span data-stu-id="b57a6-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="b57a6-117">O segundo comando carrega o certificado no $certificate para um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b57a6-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="b57a6-118">OS</span><span class="sxs-lookup"><span data-stu-id="b57a6-118">PARAMETERS</span></span>

### <span data-ttu-id="b57a6-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="b57a6-119">-CertToDeploy</span></span>
<span data-ttu-id="b57a6-120">Especifica o certificado a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="b57a6-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="b57a6-121">Você pode especificar o caminho completo de um arquivo de certificado, como um arquivo que tem um \*. cer ou \*.</span><span class="sxs-lookup"><span data-stu-id="b57a6-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="b57a6-122">extensão de nome de arquivo PFX ou um objeto de certificado X. 509.</span><span class="sxs-lookup"><span data-stu-id="b57a6-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57a6-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b57a6-123">-InformationAction</span></span>
<span data-ttu-id="b57a6-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b57a6-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b57a6-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b57a6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b57a6-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b57a6-126">Continue</span></span>
- <span data-ttu-id="b57a6-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b57a6-127">Ignore</span></span>
- <span data-ttu-id="b57a6-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="b57a6-128">Inquire</span></span>
- <span data-ttu-id="b57a6-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b57a6-129">SilentlyContinue</span></span>
- <span data-ttu-id="b57a6-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b57a6-130">Stop</span></span>
- <span data-ttu-id="b57a6-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b57a6-131">Suspend</span></span>

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

### <span data-ttu-id="b57a6-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b57a6-132">-InformationVariable</span></span>
<span data-ttu-id="b57a6-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b57a6-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b57a6-134">-Senha</span><span class="sxs-lookup"><span data-stu-id="b57a6-134">-Password</span></span>
<span data-ttu-id="b57a6-135">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="b57a6-135">Specifies the certificate password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57a6-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b57a6-136">-Profile</span></span>
<span data-ttu-id="b57a6-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b57a6-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b57a6-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b57a6-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b57a6-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b57a6-139">-ServiceName</span></span>
<span data-ttu-id="b57a6-140">Especifica o nome do serviço do Azure ao qual esse cmdlet adiciona um certificado.</span><span class="sxs-lookup"><span data-stu-id="b57a6-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57a6-141">CommonParameters</span></span>
<span data-ttu-id="b57a6-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b57a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57a6-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b57a6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57a6-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b57a6-144">INPUTS</span></span>

## <span data-ttu-id="b57a6-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b57a6-145">OUTPUTS</span></span>

### <span data-ttu-id="b57a6-146">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b57a6-146">ManagementOperationContext</span></span>

## <span data-ttu-id="b57a6-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b57a6-147">NOTES</span></span>

## <span data-ttu-id="b57a6-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b57a6-148">RELATED LINKS</span></span>

[<span data-ttu-id="b57a6-149">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b57a6-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="b57a6-150">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="b57a6-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="b57a6-151">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="b57a6-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


