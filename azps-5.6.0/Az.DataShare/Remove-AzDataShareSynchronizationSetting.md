---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: c96df19d110a795177d138b7ec34faefb72c0970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887205"
---
# <span data-ttu-id="de28f-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="de28f-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="de28f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de28f-102">SYNOPSIS</span></span>
<span data-ttu-id="de28f-103">remove uma configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="de28f-103">removes a synchronization setting</span></span>

## <span data-ttu-id="de28f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de28f-104">SYNTAX</span></span>

### <span data-ttu-id="de28f-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de28f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de28f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de28f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de28f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de28f-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de28f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de28f-108">DESCRIPTION</span></span>
<span data-ttu-id="de28f-109">O cmdlet **Remove-AzDataShareSynchronizationSetting** remove uma configuração de sincronização datashare</span><span class="sxs-lookup"><span data-stu-id="de28f-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="de28f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de28f-110">EXAMPLES</span></span>

### <span data-ttu-id="de28f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de28f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="de28f-112">Esses comandos removem uma configuração de sincronização chamada AdsShareSynchronizationSetting do share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="de28f-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="de28f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de28f-113">PARAMETERS</span></span>

### <span data-ttu-id="de28f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de28f-114">-AccountName</span></span>
<span data-ttu-id="de28f-115">Nome da conta de Compartilhamento de Dados do Azure</span><span class="sxs-lookup"><span data-stu-id="de28f-115">Azure Data Share Account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de28f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de28f-116">-AsJob</span></span>
<span data-ttu-id="de28f-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="de28f-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="de28f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de28f-118">-DefaultProfile</span></span>
<span data-ttu-id="de28f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de28f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de28f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de28f-120">-InputObject</span></span>
<span data-ttu-id="de28f-121">A configuração Sincronização de Compartilhamento de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="de28f-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de28f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="de28f-122">-Name</span></span>
<span data-ttu-id="de28f-123">Nome da configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="de28f-123">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de28f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de28f-124">-PassThru</span></span>
<span data-ttu-id="de28f-125">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="de28f-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="de28f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de28f-126">-ResourceGroupName</span></span>
<span data-ttu-id="de28f-127">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="de28f-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de28f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de28f-128">-ResourceId</span></span>
<span data-ttu-id="de28f-129">A id de recurso da configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="de28f-129">The resource id of the synchronization setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de28f-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="de28f-130">-ShareName</span></span>
<span data-ttu-id="de28f-131">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="de28f-131">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de28f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de28f-132">-Confirm</span></span>
<span data-ttu-id="de28f-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de28f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de28f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de28f-134">-WhatIf</span></span>
<span data-ttu-id="de28f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de28f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de28f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de28f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de28f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de28f-137">CommonParameters</span></span>
<span data-ttu-id="de28f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de28f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de28f-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de28f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de28f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de28f-140">INPUTS</span></span>

### <span data-ttu-id="de28f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="de28f-141">System.String</span></span>

### <span data-ttu-id="de28f-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="de28f-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="de28f-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de28f-143">OUTPUTS</span></span>

### <span data-ttu-id="de28f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de28f-144">System.Boolean</span></span>

## <span data-ttu-id="de28f-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="de28f-145">NOTES</span></span>

## <span data-ttu-id="de28f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de28f-146">RELATED LINKS</span></span>
