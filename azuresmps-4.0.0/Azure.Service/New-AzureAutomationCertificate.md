---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946222"
---
# <span data-ttu-id="ba5ce-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba5ce-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="ba5ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba5ce-102">SYNOPSIS</span></span>

<span data-ttu-id="ba5ce-103">Cria um certificado de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="ba5ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba5ce-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ba5ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba5ce-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ba5ce-106">O cmdlet **New-AzureAutomationCertificate** cria um certificado na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="ba5ce-107">Você fornece o caminho para um arquivo de certificado para carregar.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="ba5ce-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba5ce-108">EXAMPLES</span></span>

### <span data-ttu-id="ba5ce-109">Exemplo 1: criar um certificado</span><span class="sxs-lookup"><span data-stu-id="ba5ce-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="ba5ce-110">Esses comandos criam um certificado na automação do Azure chamado meu certificado.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="ba5ce-111">O primeiro comando cria a senha para o arquivo de certificado que é usado no segundo comando que cria o certificado.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="ba5ce-112">OS</span><span class="sxs-lookup"><span data-stu-id="ba5ce-112">PARAMETERS</span></span>

### <span data-ttu-id="ba5ce-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba5ce-113">-AutomationAccountName</span></span>
<span data-ttu-id="ba5ce-114">Especifica o nome da conta de automação na qual o certificado será armazenado.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5ce-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ba5ce-115">-Description</span></span>
<span data-ttu-id="ba5ce-116">Especifica uma descrição para o certificado.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-116">Specifies a description for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5ce-117">-Exportável</span><span class="sxs-lookup"><span data-stu-id="ba5ce-117">-Exportable</span></span>
<span data-ttu-id="ba5ce-118">Indica que o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5ce-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba5ce-119">-Name</span></span>
<span data-ttu-id="ba5ce-120">Especifica um nome para o certificado.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-120">Specifies a name for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5ce-121">-Senha</span><span class="sxs-lookup"><span data-stu-id="ba5ce-121">-Password</span></span>
<span data-ttu-id="ba5ce-122">Especifica a senha para o arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-122">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5ce-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="ba5ce-123">-Path</span></span>
<span data-ttu-id="ba5ce-124">Especifica o caminho para um arquivo de script para carregar.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="ba5ce-125">O arquivo pode ser. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-125">The file can be .cer or .pfx.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5ce-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ba5ce-126">-Profile</span></span>
<span data-ttu-id="ba5ce-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba5ce-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba5ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5ce-129">CommonParameters</span></span>
<span data-ttu-id="ba5ce-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5ce-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5ce-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5ce-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba5ce-132">INPUTS</span></span>

## <span data-ttu-id="ba5ce-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba5ce-133">OUTPUTS</span></span>

### <span data-ttu-id="ba5ce-134">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="ba5ce-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ba5ce-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba5ce-135">NOTES</span></span>

## <span data-ttu-id="ba5ce-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba5ce-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba5ce-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba5ce-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="ba5ce-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba5ce-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="ba5ce-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ba5ce-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


