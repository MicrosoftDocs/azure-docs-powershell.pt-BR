---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116620"
---
# <span data-ttu-id="9f049-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f049-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="9f049-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f049-102">SYNOPSIS</span></span>
<span data-ttu-id="9f049-103">Modifica a configuração de um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="9f049-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="9f049-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f049-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f049-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f049-105">DESCRIPTION</span></span>
<span data-ttu-id="9f049-106">O cmdlet **Set-AzAutomationCertificate** modifica a configuração de um certificado na Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f049-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="9f049-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f049-107">EXAMPLES</span></span>

### <span data-ttu-id="9f049-108">Exemplo 1: Modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="9f049-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9f049-109">O primeiro comando converte uma senha de texto sem forma para ser uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString texto.</span><span class="sxs-lookup"><span data-stu-id="9f049-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="9f049-110">O comando armazena esse objeto na variável $Password dados.</span><span class="sxs-lookup"><span data-stu-id="9f049-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="9f049-111">O segundo comando modifica um certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="9f049-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="9f049-112">O comando usa a senha armazenada em $Password.</span><span class="sxs-lookup"><span data-stu-id="9f049-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="9f049-113">O comando especifica o nome da conta e o caminho do arquivo carregado.</span><span class="sxs-lookup"><span data-stu-id="9f049-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="9f049-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f049-114">PARAMETERS</span></span>

### <span data-ttu-id="9f049-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f049-115">-AutomationAccountName</span></span>
<span data-ttu-id="9f049-116">Especifica o nome da conta automação para a qual este cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="9f049-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="9f049-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f049-117">-DefaultProfile</span></span>
<span data-ttu-id="9f049-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9f049-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f049-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9f049-119">-Description</span></span>
<span data-ttu-id="9f049-120">Especifica uma descrição para o certificado que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9f049-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9f049-121">-Exportável</span><span class="sxs-lookup"><span data-stu-id="9f049-121">-Exportable</span></span>
<span data-ttu-id="9f049-122">Especifica se o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="9f049-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="9f049-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f049-123">-Name</span></span>
<span data-ttu-id="9f049-124">Especifica o nome do certificado que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9f049-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9f049-125">-Senha</span><span class="sxs-lookup"><span data-stu-id="9f049-125">-Password</span></span>
<span data-ttu-id="9f049-126">Especifica a senha do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="9f049-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="9f049-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9f049-127">-Path</span></span>
<span data-ttu-id="9f049-128">Especifica o caminho para um arquivo de script a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="9f049-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="9f049-129">O arquivo pode ser um arquivo .cer ou um arquivo .pfx.</span><span class="sxs-lookup"><span data-stu-id="9f049-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="9f049-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f049-130">-ResourceGroupName</span></span>
<span data-ttu-id="9f049-131">Especifica o nome do grupo de recursos para o qual este cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="9f049-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="9f049-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f049-132">CommonParameters</span></span>
<span data-ttu-id="9f049-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f049-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f049-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f049-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f049-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f049-135">INPUTS</span></span>

### <span data-ttu-id="9f049-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9f049-136">System.String</span></span>

### <span data-ttu-id="9f049-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="9f049-137">System.Security.SecureString</span></span>

### <span data-ttu-id="9f049-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9f049-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9f049-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f049-139">OUTPUTS</span></span>

### <span data-ttu-id="9f049-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="9f049-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="9f049-141">Notas</span><span class="sxs-lookup"><span data-stu-id="9f049-141">NOTES</span></span>

## <span data-ttu-id="9f049-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f049-142">RELATED LINKS</span></span>

[<span data-ttu-id="9f049-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f049-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="9f049-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f049-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="9f049-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f049-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


