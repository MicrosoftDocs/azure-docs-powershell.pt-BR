---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 0ff167f14c9a831cb2afe2ce335a0c8bcd18acc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596685"
---
# <span data-ttu-id="525c5-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="525c5-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="525c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="525c5-102">SYNOPSIS</span></span>
<span data-ttu-id="525c5-103">Remove uma configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="525c5-103">removes a synchronization setting</span></span>

## <span data-ttu-id="525c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="525c5-104">SYNTAX</span></span>

### <span data-ttu-id="525c5-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="525c5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="525c5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="525c5-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="525c5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="525c5-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="525c5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="525c5-108">DESCRIPTION</span></span>
<span data-ttu-id="525c5-109">O cmdlet **Remove-AzDataShareSynchronizationSetting** remove uma configuração de sincronização de compartilhamento de DataShare</span><span class="sxs-lookup"><span data-stu-id="525c5-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="525c5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="525c5-110">EXAMPLES</span></span>

### <span data-ttu-id="525c5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="525c5-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="525c5-112">Esses comandos removem uma configuração de sincronização chamada AdsShareSynchronizationSetting do share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="525c5-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="525c5-113">OS</span><span class="sxs-lookup"><span data-stu-id="525c5-113">PARAMETERS</span></span>

### <span data-ttu-id="525c5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="525c5-114">-AccountName</span></span>
<span data-ttu-id="525c5-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="525c5-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="525c5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="525c5-116">-AsJob</span></span>
<span data-ttu-id="525c5-117">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="525c5-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="525c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525c5-118">-DefaultProfile</span></span>
<span data-ttu-id="525c5-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="525c5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="525c5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="525c5-120">-InputObject</span></span>
<span data-ttu-id="525c5-121">A configuração de sincronização do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="525c5-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="525c5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="525c5-122">-Name</span></span>
<span data-ttu-id="525c5-123">Nome da configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="525c5-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="525c5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="525c5-124">-PassThru</span></span>
<span data-ttu-id="525c5-125">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="525c5-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="525c5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="525c5-126">-ResourceGroupName</span></span>
<span data-ttu-id="525c5-127">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="525c5-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="525c5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="525c5-128">-ResourceId</span></span>
<span data-ttu-id="525c5-129">A ID do recurso da configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="525c5-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="525c5-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="525c5-130">-ShareName</span></span>
<span data-ttu-id="525c5-131">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="525c5-131">Azure data share name</span></span>

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

### <span data-ttu-id="525c5-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="525c5-132">-Confirm</span></span>
<span data-ttu-id="525c5-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="525c5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="525c5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="525c5-134">-WhatIf</span></span>
<span data-ttu-id="525c5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="525c5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="525c5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="525c5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="525c5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525c5-137">CommonParameters</span></span>
<span data-ttu-id="525c5-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="525c5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525c5-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="525c5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525c5-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="525c5-140">INPUTS</span></span>

### <span data-ttu-id="525c5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="525c5-141">System.String</span></span>

### <span data-ttu-id="525c5-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="525c5-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="525c5-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="525c5-143">OUTPUTS</span></span>

### <span data-ttu-id="525c5-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="525c5-144">System.Boolean</span></span>

## <span data-ttu-id="525c5-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="525c5-145">NOTES</span></span>

## <span data-ttu-id="525c5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="525c5-146">RELATED LINKS</span></span>
