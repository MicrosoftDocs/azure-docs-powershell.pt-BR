---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 3f92ebfcb9b768788b0a9acd7a1e11ef766fd22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893015"
---
# <span data-ttu-id="114e2-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="114e2-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="114e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="114e2-102">SYNOPSIS</span></span>
<span data-ttu-id="114e2-103">Cria um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="114e2-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="114e2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="114e2-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="114e2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="114e2-105">DESCRIPTION</span></span>
<span data-ttu-id="114e2-106">O cmdlet **New-AzAutomationCertificate** cria um certificado no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="114e2-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="114e2-107">Forneça o caminho para um arquivo de certificado a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="114e2-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="114e2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="114e2-108">EXAMPLES</span></span>

### <span data-ttu-id="114e2-109">Exemplo 1: Criar um novo certificado</span><span class="sxs-lookup"><span data-stu-id="114e2-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="114e2-110">O primeiro comando converte uma senha de texto simples para ser uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString de texto.</span><span class="sxs-lookup"><span data-stu-id="114e2-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="114e2-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="114e2-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="114e2-112">O segundo comando cria um certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="114e2-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="114e2-113">O comando usa a senha armazenada em $Password.</span><span class="sxs-lookup"><span data-stu-id="114e2-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="114e2-114">O comando especifica o nome da conta e o caminho do arquivo que ele carrega.</span><span class="sxs-lookup"><span data-stu-id="114e2-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="114e2-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="114e2-115">PARAMETERS</span></span>

### <span data-ttu-id="114e2-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="114e2-116">-AutomationAccountName</span></span>
<span data-ttu-id="114e2-117">Especifica o nome da conta automação para a qual esse cmdlet armazena o certificado.</span><span class="sxs-lookup"><span data-stu-id="114e2-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="114e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114e2-118">-DefaultProfile</span></span>
<span data-ttu-id="114e2-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="114e2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="114e2-120">-Description</span><span class="sxs-lookup"><span data-stu-id="114e2-120">-Description</span></span>
<span data-ttu-id="114e2-121">Especifica uma descrição do certificado.</span><span class="sxs-lookup"><span data-stu-id="114e2-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="114e2-122">-Exportable</span><span class="sxs-lookup"><span data-stu-id="114e2-122">-Exportable</span></span>
<span data-ttu-id="114e2-123">Especifica se o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="114e2-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114e2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="114e2-124">-Name</span></span>
<span data-ttu-id="114e2-125">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="114e2-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="114e2-126">-Password</span><span class="sxs-lookup"><span data-stu-id="114e2-126">-Password</span></span>
<span data-ttu-id="114e2-127">Especifica a senha do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="114e2-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="114e2-128">-Path</span><span class="sxs-lookup"><span data-stu-id="114e2-128">-Path</span></span>
<span data-ttu-id="114e2-129">Especifica o caminho para um arquivo de script que esse cmdlet carrega.</span><span class="sxs-lookup"><span data-stu-id="114e2-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="114e2-130">O arquivo pode ser um arquivo .cer ou .pfx.</span><span class="sxs-lookup"><span data-stu-id="114e2-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="114e2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="114e2-131">-ResourceGroupName</span></span>
<span data-ttu-id="114e2-132">Especifica o nome do grupo de recursos para o qual este cmdlet cria um certificado.</span><span class="sxs-lookup"><span data-stu-id="114e2-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="114e2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114e2-133">CommonParameters</span></span>
<span data-ttu-id="114e2-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114e2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114e2-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114e2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114e2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="114e2-136">INPUTS</span></span>

### <span data-ttu-id="114e2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="114e2-137">System.String</span></span>

### <span data-ttu-id="114e2-138">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="114e2-138">System.Security.SecureString</span></span>

### <span data-ttu-id="114e2-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="114e2-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="114e2-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="114e2-140">OUTPUTS</span></span>

### <span data-ttu-id="114e2-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="114e2-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="114e2-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="114e2-142">NOTES</span></span>

<span data-ttu-id="114e2-143">Esse comando deve ser executado em um computador de que você é administrador, bem como em uma sessão elevada do PowerShell; antes de o certificado ser carregado, este cmdlet usa o armazenamento X.509 local para recuperar a impressão digital e a chave, e se esse cmdlet for executado fora de uma sessão do PowerShell com elevação, você receberá um erro "Acesso negado".</span><span class="sxs-lookup"><span data-stu-id="114e2-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="114e2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="114e2-144">RELATED LINKS</span></span>

[<span data-ttu-id="114e2-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="114e2-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="114e2-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="114e2-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="114e2-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="114e2-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


