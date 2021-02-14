---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117021"
---
# <span data-ttu-id="d633f-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d633f-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="d633f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d633f-102">SYNOPSIS</span></span>
<span data-ttu-id="d633f-103">Obtém credenciais de Automação.</span><span class="sxs-lookup"><span data-stu-id="d633f-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="d633f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d633f-104">SYNTAX</span></span>

### <span data-ttu-id="d633f-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d633f-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d633f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d633f-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d633f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d633f-107">DESCRIPTION</span></span>
<span data-ttu-id="d633f-108">O cmdlet **Get-AzAutomationCredential** recebe uma ou mais credenciais de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="d633f-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="d633f-109">Por padrão, todas as credenciais são retornadas.</span><span class="sxs-lookup"><span data-stu-id="d633f-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="d633f-110">Especifique o nome de uma credencial para obter uma credencial específica.</span><span class="sxs-lookup"><span data-stu-id="d633f-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="d633f-111">Para fins de segurança, este cmdlet não retorna senhas de credenciais.</span><span class="sxs-lookup"><span data-stu-id="d633f-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="d633f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d633f-112">EXAMPLES</span></span>

### <span data-ttu-id="d633f-113">Exemplo 1: Obter todas as credenciais</span><span class="sxs-lookup"><span data-stu-id="d633f-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d633f-114">Esse comando obtém metadados para todas as credenciais da conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d633f-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d633f-115">Exemplo 2: Obter uma credencial</span><span class="sxs-lookup"><span data-stu-id="d633f-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="d633f-116">Esse comando obtém metadados para a credencial chamada ContosoCredential na conta de Automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d633f-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d633f-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d633f-117">PARAMETERS</span></span>

### <span data-ttu-id="d633f-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d633f-118">-AutomationAccountName</span></span>
<span data-ttu-id="d633f-119">Especifica o nome da conta automação para a qual este cmdlet recupera credenciais.</span><span class="sxs-lookup"><span data-stu-id="d633f-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="d633f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d633f-120">-DefaultProfile</span></span>
<span data-ttu-id="d633f-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d633f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d633f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d633f-122">-Name</span></span>
<span data-ttu-id="d633f-123">Especifica o nome de uma credencial a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="d633f-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="d633f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d633f-124">-ResourceGroupName</span></span>
<span data-ttu-id="d633f-125">Especifica o grupo de recursos para o qual este cmdlet recupera credenciais.</span><span class="sxs-lookup"><span data-stu-id="d633f-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="d633f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d633f-126">CommonParameters</span></span>
<span data-ttu-id="d633f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d633f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d633f-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d633f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d633f-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="d633f-129">INPUTS</span></span>

### <span data-ttu-id="d633f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d633f-130">System.String</span></span>

## <span data-ttu-id="d633f-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="d633f-131">OUTPUTS</span></span>

### <span data-ttu-id="d633f-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="d633f-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="d633f-133">Notas</span><span class="sxs-lookup"><span data-stu-id="d633f-133">NOTES</span></span>

## <span data-ttu-id="d633f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d633f-134">RELATED LINKS</span></span>

[<span data-ttu-id="d633f-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d633f-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="d633f-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d633f-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="d633f-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d633f-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


