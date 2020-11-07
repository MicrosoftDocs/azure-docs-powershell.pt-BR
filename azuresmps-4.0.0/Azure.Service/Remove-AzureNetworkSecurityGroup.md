---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1836F342-A05C-4402-95F7-833E50A1AB97
online version: ''
schema: 2.0.0
ms.openlocfilehash: c33d48755b731c27f12742e7c21efe39994bc751
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946154"
---
# <span data-ttu-id="75e62-101">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="75e62-101">Remove-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="75e62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75e62-102">SYNOPSIS</span></span>
<span data-ttu-id="75e62-103">Exclui um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="75e62-103">Deletes a network security group.</span></span>

## <span data-ttu-id="75e62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75e62-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroup -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="75e62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75e62-105">DESCRIPTION</span></span>
<span data-ttu-id="75e62-106">O cmdlet **Remove-AzureNetworkSecurityGroup** exclui um grupo de segurança de rede do Azure de sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="75e62-106">The **Remove-AzureNetworkSecurityGroup** cmdlet deletes an Azure network security group from your subscription.</span></span>

## <span data-ttu-id="75e62-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75e62-107">EXAMPLES</span></span>

## <span data-ttu-id="75e62-108">OS</span><span class="sxs-lookup"><span data-stu-id="75e62-108">PARAMETERS</span></span>

### <span data-ttu-id="75e62-109">-Force</span><span class="sxs-lookup"><span data-stu-id="75e62-109">-Force</span></span>
<span data-ttu-id="75e62-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="75e62-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75e62-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="75e62-111">-Name</span></span>
<span data-ttu-id="75e62-112">Especifica o nome do grupo de segurança de rede que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="75e62-112">Specifies the name of the network security group that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e62-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75e62-113">-PassThru</span></span>
<span data-ttu-id="75e62-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="75e62-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="75e62-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="75e62-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="75e62-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="75e62-116">-Profile</span></span>
<span data-ttu-id="75e62-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="75e62-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="75e62-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="75e62-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75e62-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e62-119">CommonParameters</span></span>
<span data-ttu-id="75e62-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e62-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e62-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e62-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e62-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75e62-122">INPUTS</span></span>

## <span data-ttu-id="75e62-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75e62-123">OUTPUTS</span></span>

## <span data-ttu-id="75e62-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75e62-124">NOTES</span></span>

## <span data-ttu-id="75e62-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75e62-125">RELATED LINKS</span></span>

[<span data-ttu-id="75e62-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="75e62-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="75e62-127">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="75e62-127">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)


