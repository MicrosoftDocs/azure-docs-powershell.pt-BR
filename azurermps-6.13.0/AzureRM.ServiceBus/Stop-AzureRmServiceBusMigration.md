---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/stop-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
ms.openlocfilehash: 25a8b6918c5cd10a2f47230274c357008731ffba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430852"
---
# <span data-ttu-id="d4a56-101">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d4a56-101">Stop-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="d4a56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4a56-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a56-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="d4a56-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4a56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4a56-104">SYNTAX</span></span>

### <span data-ttu-id="d4a56-105">MigrationConfigurationPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d4a56-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a56-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4a56-106">NamespaceInputObjectSet</span></span>
```
Stop-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a56-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a56-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a56-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d4a56-108">DESCRIPTION</span></span>
<span data-ttu-id="d4a56-109">Os cmdlets **Stop-AzureRmServiceBusMigration** Tremitates a migração entre o namespace padrão para Premium</span><span class="sxs-lookup"><span data-stu-id="d4a56-109">The **Stop-AzureRmServiceBusMigration** cmdlets  tremitates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="d4a56-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4a56-110">EXAMPLES</span></span>

### <span data-ttu-id="d4a56-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d4a56-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="d4a56-112">cmdlet termitates a migração entre namespace padrão e namespace Premium fornecida durante a criação da configuração de migração.</span><span class="sxs-lookup"><span data-stu-id="d4a56-112">cmdlet termitates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="d4a56-113">OS</span><span class="sxs-lookup"><span data-stu-id="d4a56-113">PARAMETERS</span></span>

### <span data-ttu-id="d4a56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a56-114">-DefaultProfile</span></span>
<span data-ttu-id="d4a56-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a56-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4a56-116">-InputObject</span></span>
<span data-ttu-id="d4a56-117">Objeto namespace padrão de configuração de migração do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="d4a56-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a56-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4a56-118">-Name</span></span>
<span data-ttu-id="d4a56-119">Nome do namespace padrão</span><span class="sxs-lookup"><span data-stu-id="d4a56-119">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a56-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4a56-120">-PassThru</span></span>
<span data-ttu-id="d4a56-121">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d4a56-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d4a56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a56-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4a56-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d4a56-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a56-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4a56-124">-ResourceId</span></span>
<span data-ttu-id="d4a56-125">ID do recurso namespace padrão de configuração de migração do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="d4a56-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a56-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d4a56-126">-Confirm</span></span>
<span data-ttu-id="d4a56-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a56-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a56-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a56-128">-WhatIf</span></span>
<span data-ttu-id="d4a56-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4a56-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a56-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4a56-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a56-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a56-131">CommonParameters</span></span>
<span data-ttu-id="d4a56-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a56-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a56-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a56-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a56-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d4a56-134">INPUTS</span></span>

### <span data-ttu-id="d4a56-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d4a56-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="d4a56-136">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4a56-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d4a56-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d4a56-137">System.String</span></span>

## <span data-ttu-id="d4a56-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d4a56-138">OUTPUTS</span></span>

### <span data-ttu-id="d4a56-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4a56-139">System.Boolean</span></span>

## <span data-ttu-id="d4a56-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d4a56-140">NOTES</span></span>

## <span data-ttu-id="d4a56-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4a56-141">RELATED LINKS</span></span>
