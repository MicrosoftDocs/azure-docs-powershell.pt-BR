---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: e82d78254e81a5b8fb98c1dfbfac2113d19361a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426824"
---
# <span data-ttu-id="04c4c-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="04c4c-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="04c4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="04c4c-103">Cria um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="04c4c-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04c4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04c4c-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c4c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="04c4c-106">O cmdlet **New-AzureRmAutomationCertificate** cria um certificado na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="04c4c-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="04c4c-107">Forneça o caminho para um arquivo de certificado para carregar.</span><span class="sxs-lookup"><span data-stu-id="04c4c-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="04c4c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04c4c-108">EXAMPLES</span></span>

### <span data-ttu-id="04c4c-109">Exemplo 1: criar um novo certificado</span><span class="sxs-lookup"><span data-stu-id="04c4c-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="04c4c-110">O primeiro comando converte uma senha de texto sem formatação para ser uma cadeia de caracteres segura usando o cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="04c4c-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="04c4c-111">O comando armazena esse objeto na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="04c4c-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="04c4c-112">O segundo comando cria um certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="04c4c-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="04c4c-113">O comando usa a senha armazenada em $Password.</span><span class="sxs-lookup"><span data-stu-id="04c4c-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="04c4c-114">O comando especifica o nome da conta e o caminho do arquivo que ele carrega.</span><span class="sxs-lookup"><span data-stu-id="04c4c-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="04c4c-115">OS</span><span class="sxs-lookup"><span data-stu-id="04c4c-115">PARAMETERS</span></span>

### <span data-ttu-id="04c4c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="04c4c-116">-AutomationAccountName</span></span>
<span data-ttu-id="04c4c-117">Especifica o nome da conta de automação para a qual esse cmdlet armazena o certificado.</span><span class="sxs-lookup"><span data-stu-id="04c4c-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="04c4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c4c-118">-DefaultProfile</span></span>
<span data-ttu-id="04c4c-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="04c4c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c4c-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="04c4c-120">-Description</span></span>
<span data-ttu-id="04c4c-121">Especifica uma descrição para o certificado.</span><span class="sxs-lookup"><span data-stu-id="04c4c-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="04c4c-122">-Exportável</span><span class="sxs-lookup"><span data-stu-id="04c4c-122">-Exportable</span></span>
<span data-ttu-id="04c4c-123">Especifica se o certificado pode ser exportado.</span><span class="sxs-lookup"><span data-stu-id="04c4c-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="04c4c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="04c4c-124">-Name</span></span>
<span data-ttu-id="04c4c-125">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="04c4c-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="04c4c-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="04c4c-126">-Password</span></span>
<span data-ttu-id="04c4c-127">Especifica a senha para o arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="04c4c-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="04c4c-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="04c4c-128">-Path</span></span>
<span data-ttu-id="04c4c-129">Especifica o caminho para um arquivo de script que o cmdlet carrega.</span><span class="sxs-lookup"><span data-stu-id="04c4c-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="04c4c-130">O arquivo pode ser um arquivo. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="04c4c-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="04c4c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c4c-131">-ResourceGroupName</span></span>
<span data-ttu-id="04c4c-132">Especifica o nome do grupo de recursos para o qual esse cmdlet cria um certificado.</span><span class="sxs-lookup"><span data-stu-id="04c4c-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="04c4c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c4c-133">CommonParameters</span></span>
<span data-ttu-id="04c4c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c4c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c4c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04c4c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c4c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04c4c-136">INPUTS</span></span>

### <span data-ttu-id="04c4c-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="04c4c-137">None</span></span>
<span data-ttu-id="04c4c-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="04c4c-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04c4c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04c4c-139">OUTPUTS</span></span>

### <span data-ttu-id="04c4c-140">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="04c4c-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="04c4c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04c4c-141">NOTES</span></span>

## <span data-ttu-id="04c4c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04c4c-142">RELATED LINKS</span></span>

[<span data-ttu-id="04c4c-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="04c4c-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="04c4c-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="04c4c-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="04c4c-145">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="04c4c-145">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


