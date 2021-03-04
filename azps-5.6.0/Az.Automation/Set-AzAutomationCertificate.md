---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 80a33fe4664e4c7814db6774e7cd427dd9a2c87e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886102"
---
# <span data-ttu-id="824e1-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="824e1-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="824e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824e1-102">SYNOPSIS</span></span>
<span data-ttu-id="824e1-103">Modifica a configuração de um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="824e1-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="824e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="824e1-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="824e1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="824e1-105">DESCRIPTION</span></span>
<span data-ttu-id="824e1-106">O cmdlet **Set-AzAutomationCertificate** modifica a configuração de um certificado no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="824e1-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="824e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="824e1-107">EXAMPLES</span></span>

### <span data-ttu-id="824e1-108">Exemplo 1: Modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="824e1-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="824e1-109">O primeiro comando converte uma senha de texto simples para ser uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString de texto.</span><span class="sxs-lookup"><span data-stu-id="824e1-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="824e1-110">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="824e1-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="824e1-111">O segundo comando modifica um certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="824e1-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="824e1-112">O comando usa a senha armazenada em $Password.</span><span class="sxs-lookup"><span data-stu-id="824e1-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="824e1-113">O comando especifica o nome da conta e o caminho do arquivo que ele carrega.</span><span class="sxs-lookup"><span data-stu-id="824e1-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="824e1-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="824e1-114">PARAMETERS</span></span>

### <span data-ttu-id="824e1-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="824e1-115">-AutomationAccountName</span></span>
<span data-ttu-id="824e1-116">Especifica o nome da conta de automação para a qual este cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="824e1-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="824e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824e1-117">-DefaultProfile</span></span>
<span data-ttu-id="824e1-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="824e1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="824e1-119">-Description</span><span class="sxs-lookup"><span data-stu-id="824e1-119">-Description</span></span>
<span data-ttu-id="824e1-120">Especifica uma descrição do certificado que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="824e1-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="824e1-121">-Exportable</span><span class="sxs-lookup"><span data-stu-id="824e1-121">-Exportable</span></span>
<span data-ttu-id="824e1-122">Especifica se o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="824e1-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="824e1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="824e1-123">-Name</span></span>
<span data-ttu-id="824e1-124">Especifica o nome do certificado que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="824e1-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="824e1-125">-Password</span><span class="sxs-lookup"><span data-stu-id="824e1-125">-Password</span></span>
<span data-ttu-id="824e1-126">Especifica a senha do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="824e1-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="824e1-127">-Path</span><span class="sxs-lookup"><span data-stu-id="824e1-127">-Path</span></span>
<span data-ttu-id="824e1-128">Especifica o caminho para um arquivo de script a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="824e1-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="824e1-129">O arquivo pode ser um arquivo .cer ou um arquivo .pfx.</span><span class="sxs-lookup"><span data-stu-id="824e1-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="824e1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="824e1-130">-ResourceGroupName</span></span>
<span data-ttu-id="824e1-131">Especifica o nome do grupo de recursos para o qual este cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="824e1-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="824e1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824e1-132">CommonParameters</span></span>
<span data-ttu-id="824e1-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824e1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824e1-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824e1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824e1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="824e1-135">INPUTS</span></span>

### <span data-ttu-id="824e1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="824e1-136">System.String</span></span>

### <span data-ttu-id="824e1-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="824e1-137">System.Security.SecureString</span></span>

### <span data-ttu-id="824e1-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="824e1-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="824e1-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="824e1-139">OUTPUTS</span></span>

### <span data-ttu-id="824e1-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="824e1-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="824e1-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="824e1-141">NOTES</span></span>

## <span data-ttu-id="824e1-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="824e1-142">RELATED LINKS</span></span>

[<span data-ttu-id="824e1-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="824e1-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="824e1-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="824e1-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="824e1-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="824e1-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


