---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 549bc5bb67eab5287bf463f7e816cc0ff597cf52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428610"
---
# <span data-ttu-id="0d5a7-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0d5a7-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="0d5a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5a7-103">Modifica a configuração de um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d5a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d5a7-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d5a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5a7-106">O cmdlet **set-AzureRmAutomationCertificate** modifica a configuração de um certificado na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="0d5a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="0d5a7-108">Exemplo 1: modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="0d5a7-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0d5a7-109">O primeiro comando converte uma senha de texto sem formatação para ser uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="0d5a7-110">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="0d5a7-111">O segundo comando modifica um certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="0d5a7-112">O comando usa a senha armazenada em $Password.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="0d5a7-113">O comando especifica o nome da conta e o caminho do arquivo que ele carrega.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="0d5a7-114">OS</span><span class="sxs-lookup"><span data-stu-id="0d5a7-114">PARAMETERS</span></span>

### <span data-ttu-id="0d5a7-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0d5a7-115">-AutomationAccountName</span></span>
<span data-ttu-id="0d5a7-116">Especifica o nome da conta de automação para a qual esse cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="0d5a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5a7-117">-DefaultProfile</span></span>
<span data-ttu-id="0d5a7-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0d5a7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d5a7-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0d5a7-119">-Description</span></span>
<span data-ttu-id="0d5a7-120">Especifica uma descrição para o certificado que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0d5a7-121">-Exportável</span><span class="sxs-lookup"><span data-stu-id="0d5a7-121">-Exportable</span></span>
<span data-ttu-id="0d5a7-122">Especifica se o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="0d5a7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d5a7-123">-Name</span></span>
<span data-ttu-id="0d5a7-124">Especifica o nome do certificado que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0d5a7-125">-Senha</span><span class="sxs-lookup"><span data-stu-id="0d5a7-125">-Password</span></span>
<span data-ttu-id="0d5a7-126">Especifica a senha para o arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="0d5a7-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="0d5a7-127">-Path</span></span>
<span data-ttu-id="0d5a7-128">Especifica o caminho para um arquivo de script para carregar.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="0d5a7-129">O arquivo pode ser um arquivo. cer ou um arquivo. pfx.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="0d5a7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d5a7-130">-ResourceGroupName</span></span>
<span data-ttu-id="0d5a7-131">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="0d5a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5a7-132">CommonParameters</span></span>
<span data-ttu-id="0d5a7-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5a7-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5a7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5a7-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d5a7-135">INPUTS</span></span>

### <span data-ttu-id="0d5a7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0d5a7-136">System.String</span></span>

### <span data-ttu-id="0d5a7-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0d5a7-137">System.Security.SecureString</span></span>

### <span data-ttu-id="0d5a7-138">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0d5a7-138">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0d5a7-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d5a7-139">OUTPUTS</span></span>

### <span data-ttu-id="0d5a7-140">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="0d5a7-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="0d5a7-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d5a7-141">NOTES</span></span>

## <span data-ttu-id="0d5a7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d5a7-142">RELATED LINKS</span></span>

[<span data-ttu-id="0d5a7-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0d5a7-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="0d5a7-144">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0d5a7-144">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="0d5a7-145">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0d5a7-145">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


