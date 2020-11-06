---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431185"
---
# <span data-ttu-id="ca5d2-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca5d2-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="ca5d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5d2-103">Importa uma configuração DSC para automação.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca5d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca5d2-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca5d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca5d2-105">DESCRIPTION</span></span>
<span data-ttu-id="ca5d2-106">O cmdlet **Import-AzureRmAutomationDscConfiguration** importa uma configuração DSC (configuração de estado desejado APS) para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="ca5d2-107">Especifique o caminho de um script APS que contém uma única configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="ca5d2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca5d2-108">EXAMPLES</span></span>

### <span data-ttu-id="ca5d2-109">Exemplo 1: importar uma configuração DSC para automação</span><span class="sxs-lookup"><span data-stu-id="ca5d2-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="ca5d2-110">Esse comando importa a configuração DSC do arquivo chamado client.ps1 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="ca5d2-111">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="ca5d2-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="ca5d2-112">Se houver uma configuração DSC existente, esse comando a substituirá.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="ca5d2-113">OS</span><span class="sxs-lookup"><span data-stu-id="ca5d2-113">PARAMETERS</span></span>

### <span data-ttu-id="ca5d2-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ca5d2-114">-AutomationAccountName</span></span>
<span data-ttu-id="ca5d2-115">Especifica o nome da conta de automação na qual esse cmdlet importa uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="ca5d2-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ca5d2-116">-Description</span></span>
<span data-ttu-id="ca5d2-117">Especifica uma descrição da configuração que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="ca5d2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ca5d2-118">-Force</span></span>
<span data-ttu-id="ca5d2-119">Indica que esse cmdlet substitui uma configuração DSC existente na automação.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5d2-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="ca5d2-120">-LogVerbose</span></span>
<span data-ttu-id="ca5d2-121">Especifica se este cmdlet ativa ou desativa o registro em log detalhado dos trabalhos de compilação dessa configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="ca5d2-122">Especifique um valor de $True para ativar o registro em log detalhado ou $False para desativá-lo.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="ca5d2-123">-Publicado</span><span class="sxs-lookup"><span data-stu-id="ca5d2-123">-Published</span></span>
<span data-ttu-id="ca5d2-124">Indica que esse cmdlet importa a configuração DSC no estado publicado.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca5d2-126">Especifica o nome de um grupo de recursos para o qual esse cmdlet importa uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="ca5d2-127">-Caminho_de_origem</span><span class="sxs-lookup"><span data-stu-id="ca5d2-127">-SourcePath</span></span>
<span data-ttu-id="ca5d2-128">Especifica o caminho do script wps_2 que contém a configuração DSC que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca5d2-129">-Marcas</span><span class="sxs-lookup"><span data-stu-id="ca5d2-129">-Tags</span></span>
<span data-ttu-id="ca5d2-130">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ca5d2-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ca5d2-131">For example:</span></span>

<span data-ttu-id="ca5d2-132">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ca5d2-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca5d2-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca5d2-133">-Confirm</span></span>
<span data-ttu-id="ca5d2-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5d2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca5d2-135">-WhatIf</span></span>
<span data-ttu-id="ca5d2-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca5d2-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5d2-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5d2-138">-DefaultProfile</span></span>
<span data-ttu-id="ca5d2-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca5d2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5d2-140">CommonParameters</span></span>
<span data-ttu-id="ca5d2-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5d2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5d2-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca5d2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5d2-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca5d2-143">INPUTS</span></span>

## <span data-ttu-id="ca5d2-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca5d2-144">OUTPUTS</span></span>

### <span data-ttu-id="ca5d2-145">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca5d2-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="ca5d2-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca5d2-146">NOTES</span></span>

## <span data-ttu-id="ca5d2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca5d2-147">RELATED LINKS</span></span>

[<span data-ttu-id="ca5d2-148">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca5d2-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="ca5d2-149">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca5d2-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
