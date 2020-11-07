---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944469"
---
# <span data-ttu-id="e98e7-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e98e7-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e98e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e98e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e98e7-103">Modifica uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="e98e7-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="e98e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e98e7-104">SYNTAX</span></span>

### <span data-ttu-id="e98e7-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="e98e7-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e98e7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e98e7-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e98e7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e98e7-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e98e7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e98e7-108">DESCRIPTION</span></span>
<span data-ttu-id="e98e7-109">O cmdlet Update-AzPowerBIEmbeddedCapacity modifica uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="e98e7-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e98e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e98e7-110">EXAMPLES</span></span>

### <span data-ttu-id="e98e7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e98e7-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="e98e7-112">Modifica a capacidade chamada testcapacity no grupo de teste de grupo de Resource para definir as marcas como key1: valor1 e Key2: value2 e administrador para testuser1@contoso.com testuser2@contoso.com e a entidade de serviço: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="e98e7-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="e98e7-113">OS</span><span class="sxs-lookup"><span data-stu-id="e98e7-113">PARAMETERS</span></span>

### <span data-ttu-id="e98e7-114">-Administrador</span><span class="sxs-lookup"><span data-stu-id="e98e7-114">-Administrator</span></span>
<span data-ttu-id="e98e7-115">Um nome separado por vírgulas para definir como administradores na capacidade.</span><span class="sxs-lookup"><span data-stu-id="e98e7-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="e98e7-116">Para a entidade de serviço: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="e98e7-116">For service principal: <service principal object id>@<tenant id></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98e7-117">-DefaultProfile</span></span>
<span data-ttu-id="e98e7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e98e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98e7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e98e7-119">-InputObject</span></span>
<span data-ttu-id="e98e7-120">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="e98e7-120">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e98e7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e98e7-121">-Name</span></span>
<span data-ttu-id="e98e7-122">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="e98e7-122">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98e7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e98e7-123">-PassThru</span></span>
<span data-ttu-id="e98e7-124">Retornará os detalhes de capacidade excluídos se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="e98e7-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="e98e7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e98e7-125">-ResourceGroupName</span></span>
<span data-ttu-id="e98e7-126">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="e98e7-126">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98e7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e98e7-127">-ResourceId</span></span>
<span data-ttu-id="e98e7-128">ResourceId da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="e98e7-128">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98e7-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="e98e7-129">-Sku</span></span>
<span data-ttu-id="e98e7-130">O nome da SKU para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="e98e7-130">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98e7-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="e98e7-131">-Tag</span></span>
<span data-ttu-id="e98e7-132">Pares de valores chave na forma de uma tabela de hash definidas como marcas na capacidade.</span><span class="sxs-lookup"><span data-stu-id="e98e7-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98e7-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e98e7-133">-Confirm</span></span>
<span data-ttu-id="e98e7-134">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="e98e7-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e98e7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e98e7-135">-WhatIf</span></span>
<span data-ttu-id="e98e7-136">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="e98e7-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e98e7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98e7-137">CommonParameters</span></span>
<span data-ttu-id="e98e7-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98e7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98e7-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e98e7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98e7-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e98e7-140">INPUTS</span></span>

### <span data-ttu-id="e98e7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e98e7-141">System.String</span></span>

### <span data-ttu-id="e98e7-142">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e98e7-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e98e7-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e98e7-143">OUTPUTS</span></span>

### <span data-ttu-id="e98e7-144">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e98e7-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e98e7-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e98e7-145">NOTES</span></span>

## <span data-ttu-id="e98e7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e98e7-146">RELATED LINKS</span></span>

[<span data-ttu-id="e98e7-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e98e7-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e98e7-148">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e98e7-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
