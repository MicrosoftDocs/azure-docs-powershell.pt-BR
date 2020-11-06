---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: c92e42f49368e894006da0f7afeb9ffcf7e4a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433340"
---
# <span data-ttu-id="7525e-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7525e-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="7525e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7525e-102">SYNOPSIS</span></span>
<span data-ttu-id="7525e-103">Obtém credenciais de automação.</span><span class="sxs-lookup"><span data-stu-id="7525e-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7525e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7525e-104">SYNTAX</span></span>

### <span data-ttu-id="7525e-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="7525e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7525e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7525e-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7525e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7525e-107">DESCRIPTION</span></span>
<span data-ttu-id="7525e-108">O cmdlet **Get-AzureRmAutomationCredential** Obtém uma ou mais credenciais de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="7525e-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="7525e-109">Por padrão, todas as credenciais são retornadas.</span><span class="sxs-lookup"><span data-stu-id="7525e-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="7525e-110">Especifique o nome de uma credencial para obter uma credencial específica.</span><span class="sxs-lookup"><span data-stu-id="7525e-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="7525e-111">Para fins de segurança, esse cmdlet não retorna senhas de credenciais.</span><span class="sxs-lookup"><span data-stu-id="7525e-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="7525e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7525e-112">EXAMPLES</span></span>

### <span data-ttu-id="7525e-113">Exemplo 1: obter todas as credenciais</span><span class="sxs-lookup"><span data-stu-id="7525e-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7525e-114">Esse comando obtém metadados de todas as credenciais na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7525e-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7525e-115">Exemplo 2: obter uma credencial</span><span class="sxs-lookup"><span data-stu-id="7525e-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="7525e-116">Esse comando obtém metadados para a credencial chamada ContosoCredential na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7525e-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7525e-117">OS</span><span class="sxs-lookup"><span data-stu-id="7525e-117">PARAMETERS</span></span>

### <span data-ttu-id="7525e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7525e-118">-AutomationAccountName</span></span>
<span data-ttu-id="7525e-119">Especifica o nome da conta de automação para a qual esse cmdlet recupera as credenciais.</span><span class="sxs-lookup"><span data-stu-id="7525e-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="7525e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7525e-120">-DefaultProfile</span></span>
<span data-ttu-id="7525e-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7525e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7525e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7525e-122">-Name</span></span>
<span data-ttu-id="7525e-123">Especifica o nome de uma credencial a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="7525e-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7525e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7525e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7525e-125">Especifica o grupo de recursos para o qual esse cmdlet recupera as credenciais.</span><span class="sxs-lookup"><span data-stu-id="7525e-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="7525e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7525e-126">CommonParameters</span></span>
<span data-ttu-id="7525e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7525e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7525e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7525e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7525e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7525e-129">INPUTS</span></span>

### <span data-ttu-id="7525e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7525e-130">System.String</span></span>

## <span data-ttu-id="7525e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7525e-131">OUTPUTS</span></span>

### <span data-ttu-id="7525e-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="7525e-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="7525e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7525e-133">NOTES</span></span>

## <span data-ttu-id="7525e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7525e-134">RELATED LINKS</span></span>

[<span data-ttu-id="7525e-135">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7525e-135">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="7525e-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7525e-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="7525e-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7525e-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


