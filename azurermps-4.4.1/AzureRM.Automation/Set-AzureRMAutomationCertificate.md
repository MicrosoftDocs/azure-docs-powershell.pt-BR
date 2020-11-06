---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 97a5db6a816b2274befde1d4efb898b0c5e2bfdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441420"
---
# <span data-ttu-id="0faf0-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0faf0-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="0faf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0faf0-102">SYNOPSIS</span></span>
<span data-ttu-id="0faf0-103">Modifica a configuração de um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="0faf0-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0faf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0faf0-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0faf0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0faf0-105">DESCRIPTION</span></span>
<span data-ttu-id="0faf0-106">O cmdlet **set-AzureRmAutomationCertificate** modifica a configuração de um certificado na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0faf0-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="0faf0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0faf0-107">EXAMPLES</span></span>

### <span data-ttu-id="0faf0-108">Exemplo 1: modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="0faf0-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0faf0-109">O primeiro comando converte uma senha de texto sem formatação para ser uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="0faf0-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="0faf0-110">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="0faf0-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="0faf0-111">O segundo comando modifica um certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="0faf0-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="0faf0-112">O comando usa a senha armazenada em $Password.</span><span class="sxs-lookup"><span data-stu-id="0faf0-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="0faf0-113">O comando especifica o nome da conta e o caminho do arquivo que ele carrega.</span><span class="sxs-lookup"><span data-stu-id="0faf0-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="0faf0-114">OS</span><span class="sxs-lookup"><span data-stu-id="0faf0-114">PARAMETERS</span></span>

### <span data-ttu-id="0faf0-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0faf0-115">-AutomationAccountName</span></span>
<span data-ttu-id="0faf0-116">Especifica o nome da conta de automação para a qual esse cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="0faf0-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0faf0-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0faf0-117">-Description</span></span>
<span data-ttu-id="0faf0-118">Especifica uma descrição para o certificado que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="0faf0-118">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0faf0-119">-Exportável</span><span class="sxs-lookup"><span data-stu-id="0faf0-119">-Exportable</span></span>
<span data-ttu-id="0faf0-120">Especifica se o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="0faf0-120">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0faf0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0faf0-121">-Name</span></span>
<span data-ttu-id="0faf0-122">Especifica o nome do certificado que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="0faf0-122">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0faf0-123">-Senha</span><span class="sxs-lookup"><span data-stu-id="0faf0-123">-Password</span></span>
<span data-ttu-id="0faf0-124">Especifica a senha para o arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="0faf0-124">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0faf0-125">-Caminho</span><span class="sxs-lookup"><span data-stu-id="0faf0-125">-Path</span></span>
<span data-ttu-id="0faf0-126">Especifica o caminho para um arquivo de script para carregar.</span><span class="sxs-lookup"><span data-stu-id="0faf0-126">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="0faf0-127">O arquivo pode ser um arquivo. cer ou um arquivo. pfx.</span><span class="sxs-lookup"><span data-stu-id="0faf0-127">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0faf0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0faf0-128">-ResourceGroupName</span></span>
<span data-ttu-id="0faf0-129">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="0faf0-129">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0faf0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0faf0-130">-DefaultProfile</span></span>
<span data-ttu-id="0faf0-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0faf0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0faf0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0faf0-132">CommonParameters</span></span>
<span data-ttu-id="0faf0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0faf0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0faf0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0faf0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0faf0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0faf0-135">INPUTS</span></span>

## <span data-ttu-id="0faf0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0faf0-136">OUTPUTS</span></span>

### <span data-ttu-id="0faf0-137">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="0faf0-137">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="0faf0-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0faf0-138">NOTES</span></span>

## <span data-ttu-id="0faf0-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0faf0-139">RELATED LINKS</span></span>

[<span data-ttu-id="0faf0-140">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0faf0-140">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="0faf0-141">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0faf0-141">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="0faf0-142">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0faf0-142">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


