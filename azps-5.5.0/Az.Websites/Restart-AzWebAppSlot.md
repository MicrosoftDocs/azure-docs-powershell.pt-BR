---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116025"
---
# <span data-ttu-id="7081d-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7081d-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="7081d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7081d-102">SYNOPSIS</span></span>

## <span data-ttu-id="7081d-103">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7081d-103">SYNTAX</span></span>

### <span data-ttu-id="7081d-104">S1</span><span class="sxs-lookup"><span data-stu-id="7081d-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7081d-105">S2</span><span class="sxs-lookup"><span data-stu-id="7081d-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7081d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7081d-106">DESCRIPTION</span></span>
<span data-ttu-id="7081d-107">O cmdlet **Restart-AzWebAppSlot** para e inicia um Slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7081d-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="7081d-108">Se o Slot do Web App estiver em um estado interrompido, use o cmdlet Start-AzWebAppSlot web app.</span><span class="sxs-lookup"><span data-stu-id="7081d-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="7081d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7081d-109">EXAMPLES</span></span>

### <span data-ttu-id="7081d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7081d-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="7081d-111">Este comando reinicia o slot Slot001 para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="7081d-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="7081d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7081d-112">PARAMETERS</span></span>

### <span data-ttu-id="7081d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7081d-113">-DefaultProfile</span></span>
<span data-ttu-id="7081d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7081d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7081d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7081d-115">-Name</span></span>
<span data-ttu-id="7081d-116">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="7081d-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7081d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7081d-117">-ResourceGroupName</span></span>
<span data-ttu-id="7081d-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7081d-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7081d-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="7081d-119">-Slot</span></span>
<span data-ttu-id="7081d-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="7081d-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7081d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7081d-121">-WebApp</span></span>
<span data-ttu-id="7081d-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="7081d-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7081d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7081d-123">CommonParameters</span></span>
<span data-ttu-id="7081d-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7081d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7081d-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7081d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7081d-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="7081d-126">INPUTS</span></span>

### <span data-ttu-id="7081d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7081d-127">System.String</span></span>

### <span data-ttu-id="7081d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7081d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7081d-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="7081d-129">OUTPUTS</span></span>

### <span data-ttu-id="7081d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7081d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7081d-131">Notas</span><span class="sxs-lookup"><span data-stu-id="7081d-131">NOTES</span></span>

## <span data-ttu-id="7081d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7081d-132">RELATED LINKS</span></span>

[<span data-ttu-id="7081d-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7081d-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="7081d-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7081d-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="7081d-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7081d-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="7081d-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7081d-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="7081d-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7081d-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="7081d-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7081d-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="7081d-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7081d-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
