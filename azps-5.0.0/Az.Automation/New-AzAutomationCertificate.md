---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281820"
---
# <span data-ttu-id="0f578-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0f578-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="0f578-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f578-102">SYNOPSIS</span></span>
<span data-ttu-id="0f578-103">Cria um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="0f578-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="0f578-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f578-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f578-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f578-105">DESCRIPTION</span></span>
<span data-ttu-id="0f578-106">O cmdlet **New-AzAutomationCertificate** cria um certificado na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f578-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="0f578-107">Forneça o caminho para um arquivo de certificado para carregar.</span><span class="sxs-lookup"><span data-stu-id="0f578-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="0f578-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f578-108">EXAMPLES</span></span>

### <span data-ttu-id="0f578-109">Exemplo 1: criar um novo certificado</span><span class="sxs-lookup"><span data-stu-id="0f578-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0f578-110">O primeiro comando converte uma senha de texto sem formatação para ser uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="0f578-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="0f578-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="0f578-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="0f578-112">O segundo comando cria um certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="0f578-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="0f578-113">O comando usa a senha armazenada em $Password.</span><span class="sxs-lookup"><span data-stu-id="0f578-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="0f578-114">O comando especifica o nome da conta e o caminho do arquivo que ele carrega.</span><span class="sxs-lookup"><span data-stu-id="0f578-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="0f578-115">OS</span><span class="sxs-lookup"><span data-stu-id="0f578-115">PARAMETERS</span></span>

### <span data-ttu-id="0f578-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0f578-116">-AutomationAccountName</span></span>
<span data-ttu-id="0f578-117">Especifica o nome da conta de automação para a qual esse cmdlet armazena o certificado.</span><span class="sxs-lookup"><span data-stu-id="0f578-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="0f578-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f578-118">-DefaultProfile</span></span>
<span data-ttu-id="0f578-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0f578-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f578-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0f578-120">-Description</span></span>
<span data-ttu-id="0f578-121">Especifica uma descrição para o certificado.</span><span class="sxs-lookup"><span data-stu-id="0f578-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="0f578-122">-Exportável</span><span class="sxs-lookup"><span data-stu-id="0f578-122">-Exportable</span></span>
<span data-ttu-id="0f578-123">Especifica se o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="0f578-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="0f578-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f578-124">-Name</span></span>
<span data-ttu-id="0f578-125">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="0f578-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="0f578-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="0f578-126">-Password</span></span>
<span data-ttu-id="0f578-127">Especifica a senha para o arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="0f578-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="0f578-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="0f578-128">-Path</span></span>
<span data-ttu-id="0f578-129">Especifica o caminho para um arquivo de script que o cmdlet carrega.</span><span class="sxs-lookup"><span data-stu-id="0f578-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="0f578-130">O arquivo pode ser um arquivo. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="0f578-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="0f578-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f578-131">-ResourceGroupName</span></span>
<span data-ttu-id="0f578-132">Especifica o nome do grupo de recursos para o qual esse cmdlet cria um certificado.</span><span class="sxs-lookup"><span data-stu-id="0f578-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="0f578-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f578-133">CommonParameters</span></span>
<span data-ttu-id="0f578-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f578-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f578-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f578-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f578-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f578-136">INPUTS</span></span>

### <span data-ttu-id="0f578-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0f578-137">System.String</span></span>

### <span data-ttu-id="0f578-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0f578-138">System.Security.SecureString</span></span>

### <span data-ttu-id="0f578-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0f578-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0f578-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f578-140">OUTPUTS</span></span>

### <span data-ttu-id="0f578-141">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="0f578-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="0f578-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f578-142">NOTES</span></span>

<span data-ttu-id="0f578-143">Esse comando deve ser executado em um computador do qual você é administrador, bem como em uma sessão do PowerShell elevada; antes de o certificado ser carregado, esse cmdlet usa a loja local X. 509 para recuperar a impressão digital e a chave e, se esse cmdlet for executado fora de uma sessão elevada do PowerShell, você receberá um erro de "acesso negado".</span><span class="sxs-lookup"><span data-stu-id="0f578-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="0f578-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f578-144">RELATED LINKS</span></span>

[<span data-ttu-id="0f578-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0f578-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="0f578-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0f578-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="0f578-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0f578-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


