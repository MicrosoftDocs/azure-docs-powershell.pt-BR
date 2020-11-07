---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946428"
---
# <span data-ttu-id="79168-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="79168-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="79168-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79168-102">SYNOPSIS</span></span>

<span data-ttu-id="79168-103">Modifica a configuração de um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="79168-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="79168-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79168-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="79168-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79168-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="79168-106">O cmdlet **set-AzureAutomationCertificate** modifica a configuração de um certificado na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="79168-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="79168-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79168-107">EXAMPLES</span></span>

### <span data-ttu-id="79168-108">Exemplo 1: atualizar um certificado</span><span class="sxs-lookup"><span data-stu-id="79168-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="79168-109">Esses comandos atualizam um certificado existente chamado myCertificate na automação.</span><span class="sxs-lookup"><span data-stu-id="79168-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="79168-110">O primeiro comando cria a senha para o arquivo de certificado que é usado no segundo comando que atualiza o certificado.</span><span class="sxs-lookup"><span data-stu-id="79168-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="79168-111">OS</span><span class="sxs-lookup"><span data-stu-id="79168-111">PARAMETERS</span></span>

### <span data-ttu-id="79168-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="79168-112">-AutomationAccountName</span></span>
<span data-ttu-id="79168-113">Especifica o nome da conta de automação com o certificado.</span><span class="sxs-lookup"><span data-stu-id="79168-113">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="79168-114">-Descrição</span><span class="sxs-lookup"><span data-stu-id="79168-114">-Description</span></span>
<span data-ttu-id="79168-115">Especifica uma descrição para o certificado.</span><span class="sxs-lookup"><span data-stu-id="79168-115">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="79168-116">-Exportável</span><span class="sxs-lookup"><span data-stu-id="79168-116">-Exportable</span></span>
<span data-ttu-id="79168-117">Indica que o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="79168-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79168-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="79168-118">-Name</span></span>
<span data-ttu-id="79168-119">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="79168-119">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="79168-120">-Senha</span><span class="sxs-lookup"><span data-stu-id="79168-120">-Password</span></span>
<span data-ttu-id="79168-121">Especifica a senha para o arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="79168-121">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="79168-122">-Caminho</span><span class="sxs-lookup"><span data-stu-id="79168-122">-Path</span></span>
<span data-ttu-id="79168-123">Especifica o caminho para um arquivo de script para carregar.</span><span class="sxs-lookup"><span data-stu-id="79168-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="79168-124">O arquivo pode ser. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="79168-124">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="79168-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="79168-125">-Profile</span></span>
<span data-ttu-id="79168-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="79168-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79168-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="79168-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79168-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79168-128">CommonParameters</span></span>
<span data-ttu-id="79168-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79168-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79168-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79168-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79168-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79168-131">INPUTS</span></span>

## <span data-ttu-id="79168-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79168-132">OUTPUTS</span></span>

### <span data-ttu-id="79168-133">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="79168-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="79168-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79168-134">NOTES</span></span>

## <span data-ttu-id="79168-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79168-135">RELATED LINKS</span></span>

[<span data-ttu-id="79168-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="79168-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="79168-137">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="79168-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="79168-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="79168-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


