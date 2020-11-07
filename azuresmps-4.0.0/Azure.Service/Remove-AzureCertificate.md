---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946167"
---
# <span data-ttu-id="25b14-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="25b14-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="25b14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25b14-102">SYNOPSIS</span></span>
<span data-ttu-id="25b14-103">Remove um certificado de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="25b14-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="25b14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25b14-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="25b14-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25b14-105">DESCRIPTION</span></span>
<span data-ttu-id="25b14-106">O cmdlet **Remove-AzureCertificate** remove um certificado de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="25b14-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="25b14-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25b14-107">EXAMPLES</span></span>

### <span data-ttu-id="25b14-108">Exemplo 1: remover um certificado de um serviço</span><span class="sxs-lookup"><span data-stu-id="25b14-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="25b14-109">Esse comando Remove o objeto de certificado que tem a impressão digital especificada do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="25b14-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="25b14-110">Exemplo 2: remover todos os certificados de um serviço</span><span class="sxs-lookup"><span data-stu-id="25b14-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="25b14-111">Esse comando obtém todos os certificados do serviço denominado ContosoService usando o cmdlet **Get-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="25b14-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="25b14-112">O comando passa cada certificado para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="25b14-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="25b14-113">Esse cmdlet Remove cada certificado do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="25b14-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="25b14-114">Exemplo 3: remover todos os certificados de um serviço que usa um algoritmo de impressão digital específico</span><span class="sxs-lookup"><span data-stu-id="25b14-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="25b14-115">Esse comando obtém todos os certificados do serviço denominado ContosoService que usam o algoritmo de impressão digital SHA1.</span><span class="sxs-lookup"><span data-stu-id="25b14-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="25b14-116">O comando passa cada certificado para o cmdlet atual, que remove cada certificado.</span><span class="sxs-lookup"><span data-stu-id="25b14-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="25b14-117">OS</span><span class="sxs-lookup"><span data-stu-id="25b14-117">PARAMETERS</span></span>

### <span data-ttu-id="25b14-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="25b14-118">-InformationAction</span></span>
<span data-ttu-id="25b14-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="25b14-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="25b14-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="25b14-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25b14-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="25b14-121">Continue</span></span>
- <span data-ttu-id="25b14-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="25b14-122">Ignore</span></span>
- <span data-ttu-id="25b14-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="25b14-123">Inquire</span></span>
- <span data-ttu-id="25b14-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="25b14-124">SilentlyContinue</span></span>
- <span data-ttu-id="25b14-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="25b14-125">Stop</span></span>
- <span data-ttu-id="25b14-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="25b14-126">Suspend</span></span>

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

### <span data-ttu-id="25b14-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="25b14-127">-InformationVariable</span></span>
<span data-ttu-id="25b14-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="25b14-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="25b14-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="25b14-129">-Profile</span></span>
<span data-ttu-id="25b14-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="25b14-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25b14-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="25b14-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25b14-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="25b14-132">-ServiceName</span></span>
<span data-ttu-id="25b14-133">Especifica o nome do serviço do Azure do qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="25b14-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="25b14-134">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="25b14-134">-Thumbprint</span></span>
<span data-ttu-id="25b14-135">Especifica a impressão digital do certificado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="25b14-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b14-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="25b14-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="25b14-137">Especifica o algoritmo que é usado para criar a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="25b14-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b14-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b14-138">CommonParameters</span></span>
<span data-ttu-id="25b14-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b14-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b14-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b14-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b14-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25b14-141">INPUTS</span></span>

## <span data-ttu-id="25b14-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25b14-142">OUTPUTS</span></span>

### <span data-ttu-id="25b14-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="25b14-143">ManagementOperationContext</span></span>

## <span data-ttu-id="25b14-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25b14-144">NOTES</span></span>

## <span data-ttu-id="25b14-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25b14-145">RELATED LINKS</span></span>

[<span data-ttu-id="25b14-146">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="25b14-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="25b14-147">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="25b14-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="25b14-148">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="25b14-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


