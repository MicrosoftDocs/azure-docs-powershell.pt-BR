---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e8d7cfcf595d7dd445d66865d922676c96b7e6d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426829"
---
# <span data-ttu-id="fb05f-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb05f-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="fb05f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb05f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb05f-103">Importa uma configuração DSC para automação.</span><span class="sxs-lookup"><span data-stu-id="fb05f-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb05f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb05f-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb05f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb05f-105">DESCRIPTION</span></span>
<span data-ttu-id="fb05f-106">O cmdlet **Import-AzureRmAutomationDscConfiguration** importa uma configuração DSC (configuração de estado desejado APS) para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb05f-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="fb05f-107">Especifique o caminho de um script APS que contém uma única configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="fb05f-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="fb05f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb05f-108">EXAMPLES</span></span>

### <span data-ttu-id="fb05f-109">Exemplo 1: importar uma configuração DSC para automação</span><span class="sxs-lookup"><span data-stu-id="fb05f-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="fb05f-110">Esse comando importa a configuração DSC do arquivo chamado client.ps1 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fb05f-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="fb05f-111">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="fb05f-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="fb05f-112">Se houver uma configuração DSC existente, esse comando a substituirá.</span><span class="sxs-lookup"><span data-stu-id="fb05f-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="fb05f-113">OS</span><span class="sxs-lookup"><span data-stu-id="fb05f-113">PARAMETERS</span></span>

### <span data-ttu-id="fb05f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fb05f-114">-AutomationAccountName</span></span>
<span data-ttu-id="fb05f-115">Especifica o nome da conta de automação na qual esse cmdlet importa uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="fb05f-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="fb05f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb05f-116">-DefaultProfile</span></span>
<span data-ttu-id="fb05f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fb05f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb05f-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="fb05f-118">-Description</span></span>
<span data-ttu-id="fb05f-119">Especifica uma descrição da configuração que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="fb05f-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="fb05f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fb05f-120">-Force</span></span>
<span data-ttu-id="fb05f-121">Indica que esse cmdlet substitui uma configuração DSC existente na automação.</span><span class="sxs-lookup"><span data-stu-id="fb05f-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb05f-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="fb05f-122">-LogVerbose</span></span>
<span data-ttu-id="fb05f-123">Especifica se este cmdlet ativa ou desativa o registro em log detalhado dos trabalhos de compilação dessa configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="fb05f-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="fb05f-124">Especifique um valor de $True para ativar o registro em log detalhado ou $False para desativá-lo.</span><span class="sxs-lookup"><span data-stu-id="fb05f-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb05f-125">-Publicado</span><span class="sxs-lookup"><span data-stu-id="fb05f-125">-Published</span></span>
<span data-ttu-id="fb05f-126">Indica que esse cmdlet importa a configuração DSC no estado publicado.</span><span class="sxs-lookup"><span data-stu-id="fb05f-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb05f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb05f-127">-ResourceGroupName</span></span>
<span data-ttu-id="fb05f-128">Especifica o nome de um grupo de recursos para o qual esse cmdlet importa uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="fb05f-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="fb05f-129">-Caminho_de_origem</span><span class="sxs-lookup"><span data-stu-id="fb05f-129">-SourcePath</span></span>
<span data-ttu-id="fb05f-130">Especifica o caminho do script wps_2 que contém a configuração DSC que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="fb05f-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb05f-131">-Marcas</span><span class="sxs-lookup"><span data-stu-id="fb05f-131">-Tags</span></span>
<span data-ttu-id="fb05f-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fb05f-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fb05f-133">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fb05f-133">For example:</span></span>

<span data-ttu-id="fb05f-134">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fb05f-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb05f-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb05f-135">-Confirm</span></span>
<span data-ttu-id="fb05f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb05f-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb05f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb05f-137">-WhatIf</span></span>
<span data-ttu-id="fb05f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb05f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb05f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb05f-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb05f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb05f-140">CommonParameters</span></span>
<span data-ttu-id="fb05f-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb05f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb05f-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb05f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb05f-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb05f-143">INPUTS</span></span>

### <span data-ttu-id="fb05f-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fb05f-144">None</span></span>
<span data-ttu-id="fb05f-145">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fb05f-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb05f-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb05f-146">OUTPUTS</span></span>

### <span data-ttu-id="fb05f-147">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb05f-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="fb05f-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb05f-148">NOTES</span></span>

## <span data-ttu-id="fb05f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb05f-149">RELATED LINKS</span></span>

[<span data-ttu-id="fb05f-150">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb05f-150">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="fb05f-151">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb05f-151">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
