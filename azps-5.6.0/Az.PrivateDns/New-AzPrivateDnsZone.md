---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: d135cc72a9830535d6b67ce80f29725a569894e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888609"
---
# <span data-ttu-id="88561-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88561-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="88561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88561-102">SYNOPSIS</span></span>
<span data-ttu-id="88561-103">Cria uma nova zona DNS privada.</span><span class="sxs-lookup"><span data-stu-id="88561-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="88561-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="88561-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88561-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="88561-105">DESCRIPTION</span></span>
<span data-ttu-id="88561-106">O cmdlet **New-AzPrivateDnsZone** cria uma nova zona DNS (Sistema de Nomes de Domínio) privada no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="88561-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="88561-107">Você deve especificar um nome de zona DNS particular exclusivo para o parâmetro *Name* ou o cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="88561-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="88561-108">Depois que a zona for criada, use o cmdlet New-AzPrivateDnsRecordSet para criar conjuntos de registros na zona.</span><span class="sxs-lookup"><span data-stu-id="88561-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="88561-109">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="88561-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="88561-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88561-110">EXAMPLES</span></span>

### <span data-ttu-id="88561-111">Exemplo 1: criar uma zona DNS privada</span><span class="sxs-lookup"><span data-stu-id="88561-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="88561-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="88561-112">PARAMETERS</span></span>

### <span data-ttu-id="88561-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88561-113">-DefaultProfile</span></span>
<span data-ttu-id="88561-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="88561-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88561-115">-Name</span><span class="sxs-lookup"><span data-stu-id="88561-115">-Name</span></span>
<span data-ttu-id="88561-116">Especifica o nome da zona DNS privada a ser criada.</span><span class="sxs-lookup"><span data-stu-id="88561-116">Specifies the name of the private DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88561-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88561-117">-ResourceGroupName</span></span>
<span data-ttu-id="88561-118">Especifica o grupo de recursos no qual criar a zona.</span><span class="sxs-lookup"><span data-stu-id="88561-118">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88561-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="88561-119">-Tag</span></span>
<span data-ttu-id="88561-120">Uma tabela de hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="88561-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="88561-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88561-121">-Confirm</span></span>
<span data-ttu-id="88561-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88561-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88561-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88561-123">-WhatIf</span></span>
<span data-ttu-id="88561-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88561-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88561-125">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88561-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88561-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88561-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88561-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88561-127">CommonParameters</span></span>
<span data-ttu-id="88561-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88561-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88561-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88561-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88561-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88561-130">INPUTS</span></span>

### <span data-ttu-id="88561-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="88561-131">None</span></span>

## <span data-ttu-id="88561-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="88561-132">OUTPUTS</span></span>

### <span data-ttu-id="88561-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88561-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="88561-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="88561-134">NOTES</span></span>

## <span data-ttu-id="88561-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88561-135">RELATED LINKS</span></span>

[<span data-ttu-id="88561-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88561-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="88561-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="88561-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="88561-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88561-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
